# Test helpers for Kohana/Symfony projects

[![Test](https://github.com/kohanaworld/testing-component/actions/workflows/tests.yaml/badge.svg)](https://github.com/kohanaworld/testing-component/actions/workflows/tests.yaml)

A collection of test helpers to ease testing of Symfony3 projects.


### The base test class

```php
<?php
use InterNations\Component\Testing\AbstractTestCase;

class MyTest extends AbstractTestCase
{
}
```

### Accessing restricted members
```php
<?php
use InterNations\Component\Testing\AccessTrait;


class MyTest ...
{
    use AccessTrait;

    public function testSomething()
    {
        $this->setNonPublicProperty($this->sut, 'privateProperty', 'value');
        $this->callNonPublicMethod($this->sut, 'protectedMethod', ['arg1', 'arg2']);
    }
}

```
