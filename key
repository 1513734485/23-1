<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>简单计算器（HTML版）</title>
    <style>
        button {
            text-align: right;
            margin-top: 10px;
            padding: 5px 10px;
        }
        label {
            display: inline-block;
            width: 60px;
            margin-top: 10px;
        }
        input, select {
            margin-top: 10px;
            padding: 3px;
        }
    </style>
</head>
<body>
    <h1>简单计算器</h1>
    
    <label>数字1</label>
    <input type="number" id="num1" placeholder="输入第一个数字">
    <br>

    <label>符号</label>
    <select id="operator">
        <option value="">请选择运算符号</option>
        <option value="+">+</option>
        <option value="-">-</option>
        <option value="*">*</option>
        <option value="/">÷</option>
    </select>
    <br>

    <label>数字2</label>
    <input type="number" id="num2" placeholder="输入第二个数字">
    <br>

    <button id="calculateBtn">结果：<span id="result"></span></button>
    <br>

    <button id="resetBtn">重置</button>

    <script>
        // 获取页面元素
        const num1Input = document.getElementById('num1');
        const num2Input = document.getElementById('num2');
        const operatorSelect = document.getElementById('operator');
        const resultSpan = document.getElementById('result');
        const calculateBtn = document.getElementById('calculateBtn');
        const resetBtn = document.getElementById('resetBtn');

        // 计算逻辑
        calculateBtn.addEventListener('click', function() {
            // 获取输入值并转为数字
            const num1 = Number(num1Input.value);
            const num2 = Number(num2Input.value);
            const operator = operatorSelect.value;
            let result = '';

            // 验证输入
            if (isNaN(num1) || isNaN(num2)) {
                result = '请输入有效数字！';
            } else if (!operator) {
                result = '请选择运算符号！';
            } else {
                // 执行对应运算
                switch (operator) {
                    case '+':
                        result = num1 + num2;
                        break;
                    case '-':
                        result = num1 - num2;
                        break;
                    case '*':
                        result = num1 * num2;
                        break;
                    case '/':
                        if (num2 === 0) {
                            result = '除数不能为0！';
                            break;
                        }
                        result = num1 / num2;
                        break;
                }
            }

            // 显示结果
            resultSpan.textContent = result;
        });

        // 重置逻辑
        resetBtn.addEventListener('click', function() {
            num1Input.value = '';
            num2Input.value = '';
            operatorSelect.value = '';
            resultSpan.textContent = '';
        });
    </script>
</body>
</html>
