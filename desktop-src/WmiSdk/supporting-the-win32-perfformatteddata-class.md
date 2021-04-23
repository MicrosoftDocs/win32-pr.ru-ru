---
description: При написании высокопроизводительного поставщика, который наследует классы из Win32 \_ перфформаттеддата, необходимо соблюдать определенные соглашения, чтобы инструментарий WMI мог вычислить значения свойств.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Поддержка класса Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702997"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="7e29c-103">Поддержка класса Win32 \_ перфформаттеддата</span><span class="sxs-lookup"><span data-stu-id="7e29c-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="7e29c-104">При написании высокопроизводительного поставщика, который наследует классы из [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), необходимо соблюдать определенные соглашения, чтобы инструментарий WMI мог вычислить значения свойств.</span><span class="sxs-lookup"><span data-stu-id="7e29c-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="7e29c-105">Создание высокопроизводительного поставщика WMI для создания счетчиков производительности не рекомендуется в любой версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="7e29c-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="7e29c-106">Дополнительные сведения см. в разделе [Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)и [библиотеках производительности и WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="7e29c-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="7e29c-107">В следующей процедуре описывается поддержка \_ класса Win32 перфформаттеддата.</span><span class="sxs-lookup"><span data-stu-id="7e29c-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="7e29c-108">**Поддержка \_ класса Win32 перфформаттеддата**</span><span class="sxs-lookup"><span data-stu-id="7e29c-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="7e29c-109">Создайте класс в том же пространстве имен, что и соответствующий необработанный класс.</span><span class="sxs-lookup"><span data-stu-id="7e29c-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="7e29c-110">Класс должен быть производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) и иметь квалификатор **HiPerf** со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="7e29c-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="7e29c-111">Дополнительные сведения о создании собственного класса для WMI см. в разделе [Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="7e29c-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="7e29c-112">Укажите "Хиперфкукер \_ v1" в квалификаторе [**поставщика**](class-qualifiers-for-performance-counter-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="7e29c-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="7e29c-113">В дополнение к квалификаторам, используемым для необработанных классов, укажите следующие квалификаторы уровня класса:</span><span class="sxs-lookup"><span data-stu-id="7e29c-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="7e29c-114">**Автокука**</span><span class="sxs-lookup"><span data-stu-id="7e29c-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-115">**\_Равкласс**</span><span class="sxs-lookup"><span data-stu-id="7e29c-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-116">**Обработанные**</span><span class="sxs-lookup"><span data-stu-id="7e29c-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-117">**Требуют**</span><span class="sxs-lookup"><span data-stu-id="7e29c-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-118">**Динамический**</span><span class="sxs-lookup"><span data-stu-id="7e29c-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="7e29c-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="7e29c-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-120">**Языкового стандарта**</span><span class="sxs-lookup"><span data-stu-id="7e29c-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-121">**перфдефаулт**</span><span class="sxs-lookup"><span data-stu-id="7e29c-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-122">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="7e29c-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-123">**Одноэлементный**</span><span class="sxs-lookup"><span data-stu-id="7e29c-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="7e29c-124">Не устанавливайте значения для **женерикперфктр**, **перфиндекс** или **хелпиндекс** , так как они будут установлены процессом ADAP.</span><span class="sxs-lookup"><span data-stu-id="7e29c-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="7e29c-125">Дополнительные сведения см. в разделе [**Квалификаторы класса для классов счетчиков производительности**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7e29c-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="7e29c-126">Включите в класс ключевое свойство с именем **Name** (это свойство не требуется для одноэлементных классов).</span><span class="sxs-lookup"><span data-stu-id="7e29c-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="7e29c-127">Значение свойства **Name** должно совпадать с соответствующим необработанным классом.</span><span class="sxs-lookup"><span data-stu-id="7e29c-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="7e29c-128">Не следует использовать ключевое свойство, кроме **Name** , в классе.</span><span class="sxs-lookup"><span data-stu-id="7e29c-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="7e29c-129">Создайте данные свойств, которые имеют тип **DWORD** (**UInt32**) или **QWORD** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="7e29c-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="7e29c-130">Свойства должны соответствовать свойству в необработанном классе или свойству в создаваемом классе.</span><span class="sxs-lookup"><span data-stu-id="7e29c-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="7e29c-131">Укажите следующие квалификаторы уровня свойств для всех свойств в классе в дополнение к квалификаторам **перфиндекс** и **перфдетаил** , используемым для свойств необработанного класса:</span><span class="sxs-lookup"><span data-stu-id="7e29c-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="7e29c-132">**Из**</span><span class="sxs-lookup"><span data-stu-id="7e29c-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-133">**кукингтипе**</span><span class="sxs-lookup"><span data-stu-id="7e29c-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-134">**Счетчик**</span><span class="sxs-lookup"><span data-stu-id="7e29c-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-135">**перфтиместамп**</span><span class="sxs-lookup"><span data-stu-id="7e29c-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-136">**перфтимефрек**</span><span class="sxs-lookup"><span data-stu-id="7e29c-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="7e29c-137">**самплевиндов**</span><span class="sxs-lookup"><span data-stu-id="7e29c-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="7e29c-138">Дополнительные сведения см. в разделе [**Квалификаторы свойств для классов счетчиков производительности**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7e29c-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="7e29c-139">Кроме того, файл заголовка Винперф. h содержит значения, которые можно указать для **перфдетаил** и **CounterType**.</span><span class="sxs-lookup"><span data-stu-id="7e29c-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="7e29c-140">Убедитесь, что поставщик отвечает [требованиям к производительности](#performance-requirements).</span><span class="sxs-lookup"><span data-stu-id="7e29c-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="7e29c-141">Требования к производительности</span><span class="sxs-lookup"><span data-stu-id="7e29c-141">Performance Requirements</span></span>

<span data-ttu-id="7e29c-142">При создании высокопроизводительного поставщика его производительность должна соответствовать следующим требованиям.</span><span class="sxs-lookup"><span data-stu-id="7e29c-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="7e29c-143">Открытие файла DLL высокой производительности может занять не более 100 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="7e29c-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="7e29c-144">В целом, открытие каждого высокопроизводительного поставщика и библиотеки производительности не может превышать 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="7e29c-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="7e29c-145">Обновление данных может занимать не более 10 миллисекунд на операцию накопления.</span><span class="sxs-lookup"><span data-stu-id="7e29c-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="7e29c-146">При общей операции обновления и получения все высокопроизводительные поставщики вместе не могут занимать более 800 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="7e29c-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="7e29c-147">Общая нагрузка ЦП для всех высокопроизводительных поставщиков не может превышать 6-7% ресурсов ЦП в интерактивном режиме или 5% для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="7e29c-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e29c-148">См. также</span><span class="sxs-lookup"><span data-stu-id="7e29c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e29c-149">Создание поставщика экземпляров в поставщике High-Performance</span><span class="sxs-lookup"><span data-stu-id="7e29c-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
