---
description: Рекомендуемый способ создания нового базового класса WMI для поставщика WMI — файл MOF-файл (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Создание базового класса WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999377"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="a148e-103">Создание базового класса WMI</span><span class="sxs-lookup"><span data-stu-id="a148e-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="a148e-104">Рекомендуемый способ создания нового базового класса WMI для поставщика WMI — файл MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a148e-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="a148e-105">Можно также создать базовый класс с помощью [API COM для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="a148e-106">Несмотря на то, что в скрипте можно создать базовый или производный класс, без поставщика, предоставляющего данные классу и его подклассам, класс не полезен.</span><span class="sxs-lookup"><span data-stu-id="a148e-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="a148e-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="a148e-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="a148e-108">Создание базового класса с помощью MOF</span><span class="sxs-lookup"><span data-stu-id="a148e-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="a148e-109">Создание базового класса с помощью C++</span><span class="sxs-lookup"><span data-stu-id="a148e-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="a148e-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a148e-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="a148e-111">Создание базового класса с помощью MOF</span><span class="sxs-lookup"><span data-stu-id="a148e-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="a148e-112">Классы WMI обычно полагаются на наследование.</span><span class="sxs-lookup"><span data-stu-id="a148e-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="a148e-113">Перед созданием базового класса проверьте классы модель CIM (CIM), доступные в распределенном управлении Task Force ([DMTF](https://www.dmtf.org/)).</span><span class="sxs-lookup"><span data-stu-id="a148e-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="a148e-114">Если многие производные классы будут использовать одни и те же свойства, помещайте эти свойства и методы в базовый класс.</span><span class="sxs-lookup"><span data-stu-id="a148e-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="a148e-115">Максимальное число свойств, которое можно определить в классе WMI, — 1024.</span><span class="sxs-lookup"><span data-stu-id="a148e-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="a148e-116">При создании базового класса Обратите внимание на приведенный ниже список правил для имен классов.</span><span class="sxs-lookup"><span data-stu-id="a148e-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="a148e-117">Используйте как прописные, так и строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="a148e-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="a148e-118">Имя класса должно начинаться с буквы.</span><span class="sxs-lookup"><span data-stu-id="a148e-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="a148e-119">Не используйте символ подчеркивания в начале или в конце.</span><span class="sxs-lookup"><span data-stu-id="a148e-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="a148e-120">Определите все остальные символы как буквы, цифры или символы подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="a148e-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="a148e-121">Используйте единообразное соглашение об именовании.</span><span class="sxs-lookup"><span data-stu-id="a148e-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="a148e-122">В отличие от этого, хорошее соглашение об именовании для класса — это два компонента, Соединенные подчеркиванием.</span><span class="sxs-lookup"><span data-stu-id="a148e-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="a148e-123">По возможности имя поставщика должно состоять из первой половины имени, а описательное имя класса должно быть второй частью.</span><span class="sxs-lookup"><span data-stu-id="a148e-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="a148e-124">Классы не могут быть изменены во время выполнения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a148e-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="a148e-125">Необходимо прерывать действие, изменить класс, а затем перезапустить службу управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a148e-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="a148e-126">Обнаружение изменения класса в настоящее время невозможно.</span><span class="sxs-lookup"><span data-stu-id="a148e-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="a148e-127">В MOF Создайте базовый класс, присвоив ему ключевое слово **Class** , но не указывая родительский класс.</span><span class="sxs-lookup"><span data-stu-id="a148e-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="a148e-128">**Создание базового класса с помощью MOF-кода**</span><span class="sxs-lookup"><span data-stu-id="a148e-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="a148e-129">Используйте ключевое слово **Class** с именем нового класса, за которым следует пара фигурных скобок и точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="a148e-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="a148e-130">Добавьте свойства и методы класса между фигурными скобками.</span><span class="sxs-lookup"><span data-stu-id="a148e-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="a148e-131">Ниже приведен пример кода.</span><span class="sxs-lookup"><span data-stu-id="a148e-131">The following code example is provided.</span></span>

    <span data-ttu-id="a148e-132">В следующем примере кода показано, как должен быть определен базовый класс.</span><span class="sxs-lookup"><span data-stu-id="a148e-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="a148e-133">В следующем примере кода показано неправильное определение базового класса.</span><span class="sxs-lookup"><span data-stu-id="a148e-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="a148e-134">Добавьте [*Квалификаторы*](gloss-q.md) любого класса перед ключевым словом class, чтобы изменить способ использования класса.</span><span class="sxs-lookup"><span data-stu-id="a148e-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="a148e-135">Поместите квалификаторы между квадратными скобками.</span><span class="sxs-lookup"><span data-stu-id="a148e-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="a148e-136">Дополнительные сведения об квалификаторах для изменения классов см. в разделе [квалификаторы WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="a148e-137">Используйте **абстрактный** квалификатор, чтобы указать, что нельзя создать экземпляр этого класса напрямую.</span><span class="sxs-lookup"><span data-stu-id="a148e-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="a148e-138">Абстрактные классы часто используются для определения свойств или методов, которые будут использоваться несколькими производными классами.</span><span class="sxs-lookup"><span data-stu-id="a148e-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="a148e-139">Дополнительные сведения см. [в разделе Создание производного класса](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="a148e-140">В следующем примере кода класс определяется как абстрактный и определяет поставщик, который будет предоставлять данные.</span><span class="sxs-lookup"><span data-stu-id="a148e-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="a148e-141">[*Разновидность*](gloss-f.md) квалификатора **ToSubClass** указывает, что сведения в квалификаторе **поставщика** наследуются производными классами.</span><span class="sxs-lookup"><span data-stu-id="a148e-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="a148e-142">Добавьте свойства и методы класса в квадратные скобки перед именем свойства или метода.</span><span class="sxs-lookup"><span data-stu-id="a148e-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="a148e-143">Дополнительные сведения см. в разделе [Добавление свойства](adding-a-property.md) и [Создание метода](creating-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="a148e-144">Эти свойства и методы можно изменить с помощью квалификаторов MOF.</span><span class="sxs-lookup"><span data-stu-id="a148e-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="a148e-145">Дополнительные сведения см. [в разделе Добавление квалификатора](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="a148e-146">В следующем примере кода показано, как изменить свойства и методы с квалификаторами MOF.</span><span class="sxs-lookup"><span data-stu-id="a148e-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="a148e-147">Сохраните MOF-файл с расширением. mof.</span><span class="sxs-lookup"><span data-stu-id="a148e-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="a148e-148">Зарегистрируйте класс в WMI, запустив [**Mofcomp.exe**](mofcomp.md) для файла.</span><span class="sxs-lookup"><span data-stu-id="a148e-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="a148e-149">**mofcomp.exe** *невмоф. mof*</span><span class="sxs-lookup"><span data-stu-id="a148e-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="a148e-150">Если не использовать параметр **-N** или \# [**пространство имен директивы pragma**](pragma-namespace.md) для указания пространства имен, скомпилированные классы MOF будут храниться в корневом \\ пространстве имен по умолчанию в репозитории.</span><span class="sxs-lookup"><span data-stu-id="a148e-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="a148e-151">Дополнительные сведения см. в разделе [**mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="a148e-152">В следующем примере кода объединены примеры MOF-кода, обсуждаемые в предыдущей процедуре, и показано, как создать базовый класс в корневом \\ пространстве имен CIMV2 с помощью MOF.</span><span class="sxs-lookup"><span data-stu-id="a148e-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="a148e-153">Дополнительные сведения см. в разделе [Создание производного класса](creating-a-derived-class.md) для примера динамического класса, производного от этого базового класса.</span><span class="sxs-lookup"><span data-stu-id="a148e-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="a148e-154">Создание базового класса с помощью C++</span><span class="sxs-lookup"><span data-stu-id="a148e-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="a148e-155">Создание базового класса с помощью API инструментария WMI является главным набором команд размещения, определяющих класс и регистрирующих класс с помощью WMI.</span><span class="sxs-lookup"><span data-stu-id="a148e-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="a148e-156">Основное назначение этого API заключается в том, чтобы позволить клиентским приложениям создавать базовые классы.</span><span class="sxs-lookup"><span data-stu-id="a148e-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="a148e-157">Однако поставщик также может использовать этот API для создания базового класса.</span><span class="sxs-lookup"><span data-stu-id="a148e-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="a148e-158">Например, если вы считаете, что MOF-код поставщика не будет установлен должным образом, вы можете указать поставщику автоматически создавать правильные классы в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="a148e-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="a148e-159">Дополнительные сведения о поставщиках см. [в разделе Написание поставщика класса](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="a148e-160">Классы не могут быть изменены во время выполнения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a148e-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="a148e-161">Необходимо прерывать действие, изменить класс, а затем перезапустить службу управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a148e-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="a148e-162">Обнаружение изменения класса в настоящее время невозможно.</span><span class="sxs-lookup"><span data-stu-id="a148e-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="a148e-163">Для правильной компиляции кода требуется следующая ссылка.</span><span class="sxs-lookup"><span data-stu-id="a148e-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="a148e-164">Новый базовый класс можно создать программно с помощью [API COM для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a148e-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="a148e-165">**Создание нового базового класса с помощью API инструментария WMI**</span><span class="sxs-lookup"><span data-stu-id="a148e-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="a148e-166">Получите определение для нового класса, вызвав метод [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) с параметром *стробжектпас* , для которого задано значение **null** .</span><span class="sxs-lookup"><span data-stu-id="a148e-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="a148e-167">В следующем примере кода показано, как получить определение для нового класса.</span><span class="sxs-lookup"><span data-stu-id="a148e-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="a148e-168">Задайте имя для класса, задав системное свойство **\_ \_ класса** с помощью вызова метода [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="a148e-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="a148e-169">В следующем примере кода показано, как присвоить имя классу, задав системное свойство **\_ \_ класса** .</span><span class="sxs-lookup"><span data-stu-id="a148e-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="a148e-170">Создайте ключевое свойство или свойства, вызвав [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="a148e-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="a148e-171">В следующем примере кода показано, как создать свойство [**index**](swbemrefreshableitem-index.md) , помеченное как ключевое свойство на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="a148e-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="a148e-172">Присоедините квалификатор [**Key**](standard-qualifiers.md) Standard к свойству ключа, вызвав метод [**Ивбемклассобжект:: жетпропертикуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) , а затем метод [**ивбемкуалифиерсет::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="a148e-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="a148e-173">В следующем примере кода показано, как присоединить квалификатор [**Key**](standard-qualifiers.md) Standard к свойству ключа.</span><span class="sxs-lookup"><span data-stu-id="a148e-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="a148e-174">Создайте другие свойства класса с помощью [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="a148e-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="a148e-175">В следующем примере кода показано, как создать дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="a148e-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="a148e-176">Зарегистрируйте новый класс, вызвав [**IWbemServices::P уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="a148e-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="a148e-177">Так как вы не можете определить ключи и индексы после регистрации нового класса, убедитесь, что все свойства определены до вызова [**путкласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="a148e-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="a148e-178">В следующем примере кода показано, как зарегистрировать новый класс.</span><span class="sxs-lookup"><span data-stu-id="a148e-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="a148e-179">В следующем примере кода объединены примеры кода, описанные в предыдущей процедуре, и показано, как создать базовый класс с помощью API WMI.</span><span class="sxs-lookup"><span data-stu-id="a148e-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="a148e-180">См. также</span><span class="sxs-lookup"><span data-stu-id="a148e-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a148e-181">Создание класса</span><span class="sxs-lookup"><span data-stu-id="a148e-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



