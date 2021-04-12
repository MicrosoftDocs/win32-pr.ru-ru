---
description: Чтобы создать метод WMI, определите входные и выходные параметры для метода.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Создание метода WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272229"
---
# <a name="creating-a-wmi-method"></a><span data-ttu-id="c6b1d-103">Создание метода WMI</span><span class="sxs-lookup"><span data-stu-id="c6b1d-103">Creating a WMI Method</span></span>

<span data-ttu-id="c6b1d-104">Чтобы создать метод WMI, определите входные и выходные параметры для метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="c6b1d-105">Входные и выходные параметры представлены специальными [**\_ \_ параметрами**](--parameters.md)системного класса WMI.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="c6b1d-106">Дополнительные сведения см. в разделе [вызов метода](calling-a-method.md) и [написание поставщика метода](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6b1d-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="c6b1d-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="c6b1d-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="c6b1d-108">Создание метода класса WMI в MOF</span><span class="sxs-lookup"><span data-stu-id="c6b1d-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="c6b1d-109">Создание метода класса WMI в C++</span><span class="sxs-lookup"><span data-stu-id="c6b1d-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="c6b1d-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c6b1d-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="c6b1d-111">Создание метода класса WMI в MOF</span><span class="sxs-lookup"><span data-stu-id="c6b1d-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="c6b1d-112">В WMI методы поставщика обычно являются отдельными действиями, относящимися к объекту, который представляет класс.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="c6b1d-113">Вместо изменения значения свойства для выполнения действия необходимо создать метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="c6b1d-114">Например, можно включить или отключить сетевой центр обработки данных (NIC), представленный [**Win32 \_ сетевого адаптера**](/windows/desktop/CIMWin32Prov/win32-networkadapter) , с помощью методов [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) и [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="c6b1d-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="c6b1d-115">Хотя эти действия могут быть представлены как свойства для чтения и записи, рекомендуется создать метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="c6b1d-116">Кроме того, если нужно сделать видимым для класса состояние или значение, рекомендуется создать свойство для чтения и записи, а не метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="c6b1d-117">В **Win32 \_ сетевого адаптера** свойство **NetEnabled** делает состояние адаптера видимым, но изменения между состояниями выполняются методами **включения** или **отключения** .</span><span class="sxs-lookup"><span data-stu-id="c6b1d-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="c6b1d-118">Объявления классов могут включать объявление одного или нескольких методов.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="c6b1d-119">Можно либо наследовать методы родительского класса, либо реализовать собственный.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="c6b1d-120">Если вы решили реализовать собственные методы, необходимо объявить метод и пометить метод специальными тегами квалификатора.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="c6b1d-121">В следующей процедуре описывается объявление метода в классе, который не наследует от базового класса.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="c6b1d-122">**Объявление метода**</span><span class="sxs-lookup"><span data-stu-id="c6b1d-122">**To declare a method**</span></span>

1.  <span data-ttu-id="c6b1d-123">Определите имя метода между фигурными скобками объявления класса, за которыми следуют все квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="c6b1d-124">В следующем примере кода описывается синтаксис метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="c6b1d-125">По завершении вставьте код MOF-файл (MOF) в репозиторий WMI, вызвав компилятор MOF.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="c6b1d-126">Дополнительные сведения см. в разделе [Компиляция MOF-файлов](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6b1d-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="c6b1d-127">В следующем списке определяются элементы объявления метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="c6b1d-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Поставщики**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="c6b1d-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-129">Связывает определенного поставщика с описанием класса.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="c6b1d-130">Значение квалификатора [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) — это имя поставщика, которое сообщает инструментарию WMI, где находится код, поддерживающий метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="c6b1d-131">Поставщик должен также отмечаться **динамическим** квалификатором любого класса, имеющего динамические экземпляры.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="c6b1d-132">В отличие от этого, не используйте **динамический** квалификатор, чтобы пометить класс, содержащий статический экземпляр, с **реализованными** методами.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Применен**</span><span class="sxs-lookup"><span data-stu-id="c6b1d-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-134">Объявляет, что вы реализуете метод, а не наследуете реализацию метода из родительского класса.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="c6b1d-135">По умолчанию WMI распространяет реализацию родительского класса в производный класс, если только производный класс не предоставляет реализацию.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="c6b1d-136">Пропуск **реализованного** квалификатора указывает, что метод не имеет реализации в этом классе.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="c6b1d-137">При повторном объявлении метода без **реализованного** квалификатора WMI по-прежнему предполагает, что вы не собираетесь реализовывать этот метод и вызываете реализацию метода родительского класса при вызове.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="c6b1d-138">Таким образом, повторное объявление метода в производном классе, не присоединяя квалификатор **Implements** , полезно только при добавлении или удалении квалификатора в метод или из него.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="c6b1d-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-140">Описывает, какое значение возвращает метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-140">Describes what value the method returns.</span></span> <span data-ttu-id="c6b1d-141">Возвращаемое значение для метода должно быть логическим, числовым, **символьным**, **строковым**, [DateTime](datetime.md)или объектом схемы.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="c6b1d-142">Можно также объявить возвращаемый тип как [void](void.md), указывая, что метод возвращает значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="c6b1d-143">Однако нельзя объявить массив как тип возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>Имя_метода</span><span class="sxs-lookup"><span data-stu-id="c6b1d-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-145">Определяет имя метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-145">Defines the name of the method.</span></span> <span data-ttu-id="c6b1d-146">Каждый метод должен иметь уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-146">Every method must have a unique name.</span></span> <span data-ttu-id="c6b1d-147">Инструментарий WMI не допускает существование двух методов с одинаковыми именами и сигнатурами в одном классе или в иерархии классов.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="c6b1d-148">Таким образом, также невозможно перегрузить метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>параметердиректион</span><span class="sxs-lookup"><span data-stu-id="c6b1d-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-150">Содержит квалификаторы, описывающие, является ли параметр входным параметром, выходным параметром или обоими.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="c6b1d-151">Не используйте одно и то же имя параметра более одного раза в качестве входного параметра или более одного раза в качестве выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="c6b1d-152">Если одно и то же имя параметра отображается одновременно с квалификаторами [**in**](standard-qualifiers.md) и **out** , то функциональность будет аналогична использованию квалификаторов **in** **и out для** одного параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="c6b1d-153">Однако при использовании отдельных объявлений входные и выходные параметры должны быть совершенно одинаковыми во всех отношениях, включая число и тип квалификаторов [**ID**](standard-wmi-qualifiers.md) , и квалификатор должен быть одинаковым и явно объявленным для обоих типов.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="c6b1d-154">Настоятельно рекомендуется использовать квалификаторы **in** и **out** в объявлении одного параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**идкуалифиер**</span><span class="sxs-lookup"><span data-stu-id="c6b1d-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-156">Содержит квалификатор [**идентификатора**](standard-wmi-qualifiers.md) , уникально определяющий расположение каждого параметра в последовательности параметров в методе.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="c6b1d-157">По умолчанию компилятор MOF автоматически помечает параметры квалификатором **идентификатора** .</span><span class="sxs-lookup"><span data-stu-id="c6b1d-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="c6b1d-158">Компилятор помечает первый параметр значением 0 (ноль), второй параметр — значением 1 (один) и т. д.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="c6b1d-159">При необходимости можно явно указать последовательность ИДЕНТИФИКАТОРов в коде MOF.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span><span class="sxs-lookup"><span data-stu-id="c6b1d-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-161">Описывает тип данных, который может принимать метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="c6b1d-162">Тип параметра можно определить как любое значение типа данных MOF, включая массив, объект схемы или ссылку.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="c6b1d-163">При использовании массива в качестве параметра используйте массив как несвязанный или с явно заданным размером.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="c6b1d-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span><span class="sxs-lookup"><span data-stu-id="c6b1d-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="c6b1d-165">Содержит имя параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-165">Contains the name of the parameter.</span></span> <span data-ttu-id="c6b1d-166">На этом этапе можно также задать значение по умолчанию для параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="c6b1d-167">Параметры, у которых нет начальных значений, остаются неназначенными.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="c6b1d-168">В следующем примере кода описывается список параметров и квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-168">The following code example describes parameter listing and qualifiers.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

<span data-ttu-id="c6b1d-169">В следующем примере кода показано, как использовать массив в параметре MOF.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-169">The following code example describes how to use an array in a MOF parameter.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

<span data-ttu-id="c6b1d-170">В следующем примере кода описывается использование объекта схемы в качестве параметра и возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

<span data-ttu-id="c6b1d-171">В следующем примере кода показано, как включить две ссылки: одну для экземпляра класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , а другую — для экземпляра неизвестного типа объекта.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="c6b1d-172">Создание метода класса WMI в C++</span><span class="sxs-lookup"><span data-stu-id="c6b1d-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="c6b1d-173">Следующая процедура описывает, как создать метод класса WMI программным способом.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="c6b1d-174">**Создание метода класса WMI программным способом**</span><span class="sxs-lookup"><span data-stu-id="c6b1d-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="c6b1d-175">Создайте класс, которому будет принадлежать метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="c6b1d-176">Сначала необходимо создать класс для размещения метода перед созданием метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="c6b1d-177">Получите два дочерних класса системного класса [**\_ \_ Parameters**](--parameters.md) с помощью [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="c6b1d-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="c6b1d-178">Используйте первый дочерний класс для описания входных параметров, а второй — для описания параметров out.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="c6b1d-179">При необходимости можно выполнить одно извлечение, за которым следует вызов метода [**ивбемклассобжект:: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .</span><span class="sxs-lookup"><span data-stu-id="c6b1d-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="c6b1d-180">Запишите входные параметры в первый класс и выходные параметры второго класса, используя один или несколько вызовов [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="c6b1d-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="c6b1d-181">При описании параметров для метода обратите внимание на следующие правила и ограничения.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="c6b1d-182">Обрабатывать \[ входные \] параметры как отдельные записи, один в объекте, который содержит параметры In, и один в объекте, который содержит параметры out.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="c6b1d-183">Остальные \[ \] квалификаторы, кроме квалификаторов in, должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="c6b1d-184">Укажите квалификаторы [**идентификатора**](standard-wmi-qualifiers.md) , начиная с 0 (нуль), по одному для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="c6b1d-185">Порядок входных или выходных параметров устанавливается значением квалификатора [**ID**](standard-wmi-qualifiers.md) для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="c6b1d-186">Все входные аргументы должны предшествовать любым выходным аргументам.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="c6b1d-187">Изменение порядка входных и выходных параметров метода при обновлении существующего поставщика методов может привести к сбою в приложениях, вызывающих этот метод.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="c6b1d-188">Добавьте новые входные параметры в конец существующих параметров вместо того, чтобы вставлять их в уже установленную последовательность.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="c6b1d-189">Не забудьте оставить пробелы в последовательности квалификаторов [**идентификаторов**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="c6b1d-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="c6b1d-190">Поместите возвращаемое значение в класс out-Parameters в качестве свойства с именем **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="c6b1d-191">Это определяет свойство как возвращаемое значение метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="c6b1d-192">CIM-тип этого свойства является типом возвращаемого значения метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="c6b1d-193">Если метод имеет тип возвращаемого значения void, свойство **ReturnValue** не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="c6b1d-194">Кроме того, свойство **ReturnValue** не может иметь квалификатор [**идентификатора**](standard-wmi-qualifiers.md) , как и аргументы метода.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="c6b1d-195">Назначение квалификатора **идентификатора** свойству **RETURNVALUE** вызывает ошибку WMI.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="c6b1d-196">Выражать значения всех параметров по умолчанию для свойства в классе.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="c6b1d-197">Поместите оба объекта [**\_ \_ параметров**](--parameters.md) в родительский класс с помощью вызова [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="c6b1d-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="c6b1d-198">Один вызов [**путмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) может поместить оба объекта [**\_ \_ параметров**](--parameters.md) в класс.</span><span class="sxs-lookup"><span data-stu-id="c6b1d-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6b1d-199">См. также</span><span class="sxs-lookup"><span data-stu-id="c6b1d-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6b1d-200">Создание класса</span><span class="sxs-lookup"><span data-stu-id="c6b1d-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 
