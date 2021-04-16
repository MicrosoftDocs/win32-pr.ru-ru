---
description: При написании высокопроизводительного поставщика, который наследует классы из Win32 \_ перфравдата, необходимо соблюдать определенные соглашения, чтобы инструментарий WMI мог передать данные в значения свойств.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Поддержка класса Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650658"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="46e21-103">Поддержка класса Win32 \_ перфравдата</span><span class="sxs-lookup"><span data-stu-id="46e21-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="46e21-104">При написании высокопроизводительного поставщика, который наследует классы из [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), необходимо соблюдать определенные соглашения, чтобы инструментарий WMI мог передать данные в значения свойств.</span><span class="sxs-lookup"><span data-stu-id="46e21-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="46e21-105">Создание высокопроизводительного поставщика WMI для создания счетчиков производительности не рекомендуется в любой версии операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="46e21-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="46e21-106">Дополнительные сведения см. в разделе [Создание поставщика экземпляров в поставщике High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)и [библиотеках производительности и WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="46e21-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="46e21-107">В следующей процедуре описывается поддержка класса [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) в высокопроизводительном поставщике.</span><span class="sxs-lookup"><span data-stu-id="46e21-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="46e21-108">**Поддержка \_ класса Win32 перфравдата**</span><span class="sxs-lookup"><span data-stu-id="46e21-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="46e21-109">Создайте класс в корневом \\ пространстве имен CIMv2.</span><span class="sxs-lookup"><span data-stu-id="46e21-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="46e21-110">Класс должен быть производным от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и иметь квалификатор **HiPerf** со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="46e21-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="46e21-111">Можно также добавить классы данных производительности WDM (driver) в корневое \\ пространство имен WMI.</span><span class="sxs-lookup"><span data-stu-id="46e21-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="46e21-112">Дополнительные сведения о создании собственного класса для WMI см. в разделе [Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="46e21-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="46e21-113">В квалификаторе поставщика укажите для поставщика значение "преобразовать права NT5 \_ женерикперфпровидер \_ v1". </span><span class="sxs-lookup"><span data-stu-id="46e21-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="46e21-114">Укажите следующие квалификаторы уровня класса:</span><span class="sxs-lookup"><span data-stu-id="46e21-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="46e21-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="46e21-115">**HiPerf**</span></span>
    -   <span data-ttu-id="46e21-116">**Локаль**</span><span class="sxs-lookup"><span data-stu-id="46e21-116">**Locale**</span></span>
    -   <span data-ttu-id="46e21-117">**перфдетаил**</span><span class="sxs-lookup"><span data-stu-id="46e21-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="46e21-118">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="46e21-118">**Provider**</span></span>

    <span data-ttu-id="46e21-119">Дополнительные сведения см. в разделе [**Квалификаторы класса для классов счетчиков производительности**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="46e21-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="46e21-120">Не определяйте квалификатор **женерикперфктр** , так как он зарезервирован для процесса ADAP, который передает данные библиотеки производительности в классы WMI.</span><span class="sxs-lookup"><span data-stu-id="46e21-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="46e21-121">Заполните соответствующие свойства timestamp и Frequency, используемые для вычисления формул типа счетчика.</span><span class="sxs-lookup"><span data-stu-id="46e21-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="46e21-122">Эти свойства наследуются от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , и при написании высокопроизводительного поставщика необходимо заполнить их, чтобы класс отображался в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="46e21-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="46e21-123">Включите в класс ключевое свойство с именем **Name** (это свойство не требуется для одноэлементных классов).</span><span class="sxs-lookup"><span data-stu-id="46e21-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="46e21-124">Не следует использовать ключевое свойство, кроме **Name** , в классе.</span><span class="sxs-lookup"><span data-stu-id="46e21-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="46e21-125">Создайте свойства с типом данных **DWORD** (**UInt32**) или **QWORD** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="46e21-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="46e21-126">Эти свойства становятся счетчиками производительности при передаче в библиотеки производительности.</span><span class="sxs-lookup"><span data-stu-id="46e21-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="46e21-127">Укажите следующие квалификаторы уровня свойств для всех свойств в классе:</span><span class="sxs-lookup"><span data-stu-id="46e21-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="46e21-128">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="46e21-128">**DisplayName**</span></span>
    -   <span data-ttu-id="46e21-129">**CounterType**</span><span class="sxs-lookup"><span data-stu-id="46e21-129">**CounterType**</span></span>
    -   <span data-ttu-id="46e21-130">**дефаултскале**</span><span class="sxs-lookup"><span data-stu-id="46e21-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="46e21-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46e21-131">**Description**</span></span>
    -   <span data-ttu-id="46e21-132">**перфдефаулт**</span><span class="sxs-lookup"><span data-stu-id="46e21-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="46e21-133">**перфдетаил**</span><span class="sxs-lookup"><span data-stu-id="46e21-133">**PerfDetail**</span></span>

    <span data-ttu-id="46e21-134">Дополнительные сведения см. в разделе [**Квалификаторы свойств для классов счетчиков производительности**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="46e21-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="46e21-135">Кроме того, файл заголовка Винперф. h содержит значения, которые можно указать для **перфдетаил** и **CounterType**.</span><span class="sxs-lookup"><span data-stu-id="46e21-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="46e21-136">Инструментарий WMI использует квалификаторы **DisplayName**, **locale** и **Description** для локализации.</span><span class="sxs-lookup"><span data-stu-id="46e21-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="46e21-137">Необходимо добавить измененные квалификаторы в \_ пространство имен MS 409 (на английском языке), чтобы системный монитор мог правильно отображать данные класса.</span><span class="sxs-lookup"><span data-stu-id="46e21-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="46e21-138">Это означает, что вы измените определение свойства, добавив квалификатор **Description** с пояснительным текстом и заполнив значение **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="46e21-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="46e21-139">Кроме того, необходимо добавить измененные квалификаторы в любое другое пространство имен языкового стандарта, поддерживаемое вашим классом.</span><span class="sxs-lookup"><span data-stu-id="46e21-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="46e21-140">Если пользователь запрашивает данные из языкового стандарта, для которого не предоставлены измененные квалификаторы, WMI по умолчанию принимает определения, указанные в \_ пространстве имен MS 409.</span><span class="sxs-lookup"><span data-stu-id="46e21-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="46e21-141">Создайте базовое свойство для любого свойства, имеющего тип счетчика, ожидающего базового значения.</span><span class="sxs-lookup"><span data-stu-id="46e21-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="46e21-142">Это свойство следует непосредственно за свойством и называется \* PropertyName \***\_ base**.</span><span class="sxs-lookup"><span data-stu-id="46e21-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="46e21-143">Например, для вычисления числа выборок в среднем свойству **авгдискбитесперреад** в классе [**\_ \_ \_ LogicalDisk Win32 перфравдата перфдиск**](./retrieving-raw-and-formatted-performance-data.md) требуется базовое свойство с именем **авгдискбитесперреад \_ base** .</span><span class="sxs-lookup"><span data-stu-id="46e21-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="46e21-144">Чтобы определить, требуется ли для используемого типа счетчика базовое свойство, найдите тип счетчика по имени или десятичному значению в списке [типы счетчиков производительности WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="46e21-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="46e21-145">Убедитесь, что поставщик отвечает [требованиям к производительности](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="46e21-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="46e21-146">См. также</span><span class="sxs-lookup"><span data-stu-id="46e21-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46e21-147">Создание поставщика экземпляров в поставщике High-Performance</span><span class="sxs-lookup"><span data-stu-id="46e21-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
