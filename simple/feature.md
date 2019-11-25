正如我们知道的，behave是基于行为的测试，首先我们要建立自然语言来对我们测试的用例进行行为的描述。

比如我们现在要测试behave是否正确安装：

`behave_installed.feature`
```gherkin
# file:features/behave_installed.feature
Feature: Showing off behave

Scenario: Run a simple test
    Given we have behave installed
    When we implement a test
    Then behave will test it for us!
```
**Given**

这一个描述理解为是设定一个环境。

**When**

这一个描述就是为我们的用例来限定条件。

**Then**

这一个描述是我们所看的结果。


OK，第一步我们已经做完了，我们开始实现测试。实现测试简单，在.feature相同目录下建立一个steps目录，在此目录中新建一个与.feature同名的.py文件。如下：

```python
# file:features/steps/behave_installed.py
# ----------------------------------------------------------------------------
# STEPS:
# ----------------------------------------------------------------------------
from behave import given, when, then


@given('we have behave installed')
def step_impl(context):
    pass


@when('we implement a test')
def step_impl(context):
    assert True is not False


@then('behave will test it for us!')
def step_impl(context):
    assert context.failed is False
```