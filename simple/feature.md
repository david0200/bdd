正如我们知道的，behave是基于行为的测试，首先我们要建立自然语言来对我们测试的用例进行行为的描述。

比如：

`behave_installed.feature`
```gherkin
# file:features/behave_installed.feature
Feature: Showing off behave

Scenario: Run a simple test
    Given we have behave installed
    When we implement a test
    Then behave will test it for us!
```