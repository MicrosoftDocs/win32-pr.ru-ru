---
description: Создание производного класса в WMI очень похоже на создание базового класса. Как и в случае с базовым классом, необходимо сначала определить производный класс, а затем зарегистрировать производный класс с помощью WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Создание производного класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711748"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="a93d9-104">Создание производного класса WMI</span><span class="sxs-lookup"><span data-stu-id="a93d9-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="a93d9-105">Создание производного класса в WMI очень похоже на создание базового класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="a93d9-106">Как и в случае с базовым классом, необходимо сначала определить производный класс, а затем зарегистрировать производный класс с помощью WMI.</span><span class="sxs-lookup"><span data-stu-id="a93d9-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="a93d9-107">Основное отличие заключается в том, что сначала необходимо определить родительский класс, из которого требуется выполнить наследование.</span><span class="sxs-lookup"><span data-stu-id="a93d9-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="a93d9-108">Дополнительные сведения см. в разделе [написание поставщика класса](writing-a-class-provider.md) и [написание поставщика экземпляра](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a93d9-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="a93d9-109">Рекомендуемый способ создания классов для поставщика — MOF-файл (MOF) файлов.</span><span class="sxs-lookup"><span data-stu-id="a93d9-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="a93d9-110">Несколько производных классов, связанных друг с другом, должны быть сгруппированы в MOF-файл вместе с любыми базовыми классами, из которых они наследуют свойства или методы.</span><span class="sxs-lookup"><span data-stu-id="a93d9-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="a93d9-111">При помещении каждого класса в отдельный MOF-файл каждый файл должен быть скомпилирован, прежде чем поставщик сможет правильно работать.</span><span class="sxs-lookup"><span data-stu-id="a93d9-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="a93d9-112">После создания класса необходимо удалить все экземпляры класса, прежде чем можно будет выполнять следующие действия в производном классе:</span><span class="sxs-lookup"><span data-stu-id="a93d9-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="a93d9-113">Измените родительский класс производного класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="a93d9-114">Добавление или удаление свойств.</span><span class="sxs-lookup"><span data-stu-id="a93d9-114">Add or remove properties.</span></span>
-   <span data-ttu-id="a93d9-115">Измените типы свойств.</span><span class="sxs-lookup"><span data-stu-id="a93d9-115">Change property types.</span></span>
-   <span data-ttu-id="a93d9-116">Добавление или удаление [**ключа**](key-qualifier.md) или **индексированных** квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="a93d9-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="a93d9-117">Добавление или удаление [**одноэлементных**](standard-wmi-qualifiers.md), **динамических** или [**абстрактных**](standard-qualifiers.md) квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="a93d9-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="a93d9-118">Чтобы добавить, удалить или изменить свойство или квалификатор, вызовите [**IWbemServices::P уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) или [**\_ SWbemObject.**](swbemobject-put-.md) Set и установите для параметра flag значение "Force Mode".</span><span class="sxs-lookup"><span data-stu-id="a93d9-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="a93d9-119">[**Абстрактный**](standard-qualifiers.md) квалификатор можно использовать только в том случае, если родительский класс является абстрактным.</span><span class="sxs-lookup"><span data-stu-id="a93d9-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="a93d9-120">При объявлении производного класса Обратите внимание на следующие правила и ограничения.</span><span class="sxs-lookup"><span data-stu-id="a93d9-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="a93d9-121">Родительский класс производного класса должен уже существовать.</span><span class="sxs-lookup"><span data-stu-id="a93d9-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="a93d9-122">Объявление родительского класса может находиться в том же MOF-файле, что и производный класс, или в другом файле.</span><span class="sxs-lookup"><span data-stu-id="a93d9-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="a93d9-123">Если родительский класс неизвестен, компилятор создает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="a93d9-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="a93d9-124">Производный класс может иметь только один родительский класс.</span><span class="sxs-lookup"><span data-stu-id="a93d9-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="a93d9-125">Инструментарий WMI не поддерживает множественное наследование.</span><span class="sxs-lookup"><span data-stu-id="a93d9-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="a93d9-126">Однако у родительского класса может быть множество производных классов.</span><span class="sxs-lookup"><span data-stu-id="a93d9-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="a93d9-127">Можно определить индексы для производных классов, но WMI не использует эти индексы.</span><span class="sxs-lookup"><span data-stu-id="a93d9-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="a93d9-128">Поэтому указание индекса в производном классе не повышает производительность запросов экземпляров производного класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="a93d9-129">Можно повысить производительность запроса в производном классе, указав индексированные свойства для родительского класса производного класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="a93d9-130">Определения производных классов могут быть более сложными и могут включать такие функции, как псевдонимы, квалификаторы и разновидности квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="a93d9-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="a93d9-131">Дополнительные сведения см. в разделе [Создание псевдонима](creating-an-alias.md) и [Добавление квалификатора](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="a93d9-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="a93d9-132">Если вы хотите изменить квалификатор, измените значение свойства базового класса по умолчанию или более строго введите ссылку или внедренное свойство объекта базового класса, необходимо снова объявить весь базовый класс.</span><span class="sxs-lookup"><span data-stu-id="a93d9-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="a93d9-133">Максимальное число свойств, которое можно определить в классе WMI, — 1024.</span><span class="sxs-lookup"><span data-stu-id="a93d9-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="a93d9-134">Классы не могут быть изменены во время выполнения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a93d9-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="a93d9-135">Необходимо прерывать действие, изменить класс, а затем перезапустить службу управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a93d9-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="a93d9-136">Обнаружение изменения класса в настоящее время невозможно.</span><span class="sxs-lookup"><span data-stu-id="a93d9-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="a93d9-137">Как и в случае с базовым классом, наиболее распространенным применением этого метода будет клиентские приложения.</span><span class="sxs-lookup"><span data-stu-id="a93d9-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="a93d9-138">Однако поставщик может также создать производный класс.</span><span class="sxs-lookup"><span data-stu-id="a93d9-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="a93d9-139">Дополнительные сведения см. в разделе [Создание базового класса](creating-a-base-class.md) и [запись поставщика класса](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a93d9-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="a93d9-140">В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.</span><span class="sxs-lookup"><span data-stu-id="a93d9-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="a93d9-141">В следующей процедуре описывается создание производного класса с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="a93d9-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="a93d9-142">**Создание производного класса с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="a93d9-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="a93d9-143">Нахождение базового класса с вызовом [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="a93d9-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="a93d9-144">В следующем примере кода показано, как можно разместить пример базового класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="a93d9-145">Создайте производный объект из базового класса с помощью вызова [**ивбемклассобжект:: спавндериведкласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span><span class="sxs-lookup"><span data-stu-id="a93d9-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="a93d9-146">В следующем примере кода показано, как создать объект производного класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="a93d9-147">Задайте имя для класса, задав системное свойство **\_ \_ класса** с помощью вызова метода [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="a93d9-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="a93d9-148">В следующем примере кода показано, как присвоить имя производному классу.</span><span class="sxs-lookup"><span data-stu-id="a93d9-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="a93d9-149">Создайте дополнительные свойства с помощью [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="a93d9-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="a93d9-150">В следующем примере кода показано, как создать дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="a93d9-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="a93d9-151">Сохраните новый класс, вызвав [**IWbemServices::P уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="a93d9-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="a93d9-152">В следующем примере кода показано, как сохранить новый производный класс.</span><span class="sxs-lookup"><span data-stu-id="a93d9-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="a93d9-153">Следующий пример кода сочетает примеры кода, описанные в предыдущей процедуре, чтобы описать, как создать производный класс с помощью API WMI.</span><span class="sxs-lookup"><span data-stu-id="a93d9-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="a93d9-154">В следующей процедуре описывается определение производного класса с помощью MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a93d9-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="a93d9-155">**Определение производного класса с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="a93d9-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="a93d9-156">Определите производный класс с помощью ключевого слова **Class** , укажите имя производного класса и имя родительского класса, разделенное двоеточием.</span><span class="sxs-lookup"><span data-stu-id="a93d9-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="a93d9-157">В следующем примере кода описывается реализация производного класса.</span><span class="sxs-lookup"><span data-stu-id="a93d9-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="a93d9-158">По завершении Скомпилируйте MOF-код с помощью компилятора MOF.</span><span class="sxs-lookup"><span data-stu-id="a93d9-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="a93d9-159">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="a93d9-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a93d9-160">См. также</span><span class="sxs-lookup"><span data-stu-id="a93d9-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a93d9-161">Создание класса</span><span class="sxs-lookup"><span data-stu-id="a93d9-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



