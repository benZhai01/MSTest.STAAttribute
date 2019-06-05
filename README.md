# MSTest.STAAttribute

Using STATestMethod instead of TestMethod for Net Core project:

```C#
[TestClass]
public class TestClass1
{
    [STATestMethod]
    public void Test_STA()
    {
        Assert.AreEqual(ApartmentState.STA, Thread.CurrentThread.GetApartmentState());
    }
}
```

Using STATestMethod instead of TestMethod for Net Core project:

```C#
[STATestClass]
public class TestClass1
{
    [TestMethod]
    public void Test1()
    {
        Assert.AreEqual(ApartmentState.STA, Thread.CurrentThread.GetApartmentState());
    }

    [STATestMethod]
    public void Test2()
    {
        Assert.AreEqual(ApartmentState.STA, Thread.CurrentThread.GetApartmentState());
    }

}
```