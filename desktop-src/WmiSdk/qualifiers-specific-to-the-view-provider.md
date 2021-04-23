---
description: Ниже перечислены квалификаторы, используемые для определения классов поставщиков представления.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Квалификаторы, относящиеся к поставщику представления
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265878"
---
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="9f609-103">Квалификаторы, относящиеся к поставщику представления</span><span class="sxs-lookup"><span data-stu-id="9f609-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="9f609-104">Ниже перечислены квалификаторы, используемые для определения классов поставщиков представления.</span><span class="sxs-lookup"><span data-stu-id="9f609-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="9f609-105">Класс поставщика представления поддерживает только NetBIOS-имена при использовании удаленных ссылок.</span><span class="sxs-lookup"><span data-stu-id="9f609-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="9f609-106">Если в удаленной ссылке используется IP-адрес или имя DNS, соединение завершается с ошибкой 0x800706BA.</span><span class="sxs-lookup"><span data-stu-id="9f609-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="9f609-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Направлений**</span><span class="sxs-lookup"><span data-stu-id="9f609-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="9f609-108">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9f609-108">Data type: **boolean**</span></span>

<span data-ttu-id="9f609-109">Используется со свойствами сопоставления представлений для предотвращения сопоставления ссылок на представление со ссылками на представления.</span><span class="sxs-lookup"><span data-stu-id="9f609-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="9f609-110">В следующем примере свойство **GroupComponent** определяется как ссылка на ассоциацию, которая не сопоставлена со ссылкой на представление.</span><span class="sxs-lookup"><span data-stu-id="9f609-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="9f609-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**хиддендефаулт**</span><span class="sxs-lookup"><span data-stu-id="9f609-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="9f609-112">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9f609-112">Data type: **boolean**</span></span>

<span data-ttu-id="9f609-113">Значение по умолчанию для свойства класса представления на основе свойства исходного класса с другим значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f609-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="9f609-114">Базовый класс источника подразумевается представлением.</span><span class="sxs-lookup"><span data-stu-id="9f609-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="9f609-115">Например, исходный класс [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) имеет [логическое](boolean.md) свойство **рунрепеатедли** , которое указывает, должно ли задание выполняться периодически или только один раз.</span><span class="sxs-lookup"><span data-stu-id="9f609-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="9f609-116">Значение по умолчанию **рунрепеатедли** не равно true для **Win32 \_ ScheduledJob**, но имеет значение true для класса View.</span><span class="sxs-lookup"><span data-stu-id="9f609-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span data-ttu-id="9f609-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**жоинон**</span><span class="sxs-lookup"><span data-stu-id="9f609-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="9f609-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f609-118">Data type: **string**</span></span>

<span data-ttu-id="9f609-119">Определяет, как присоединяются экземпляры исходного класса в классах представления соединения.</span><span class="sxs-lookup"><span data-stu-id="9f609-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="9f609-120">В следующем примере показано, как использовать квалификатор **жоинон** для объединения двух исходных классов.</span><span class="sxs-lookup"><span data-stu-id="9f609-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="9f609-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**месодсаурце**</span><span class="sxs-lookup"><span data-stu-id="9f609-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="9f609-122">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="9f609-122">Data type: **string array**</span></span>

<span data-ttu-id="9f609-123">Исходный метод для выполнения метода представления.</span><span class="sxs-lookup"><span data-stu-id="9f609-123">Source method to execute for the view method.</span></span> <span data-ttu-id="9f609-124">Аналогичные инструкции см. в разделе [квалификатор пропертисаурцес](propertysources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="9f609-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="9f609-125">Сигнатура метода должна точно соответствовать сигнатуре исходного класса.</span><span class="sxs-lookup"><span data-stu-id="9f609-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="9f609-126">Скопируйте сигнатуру метода из MOF-файла, определяющего исходный класс.</span><span class="sxs-lookup"><span data-stu-id="9f609-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="9f609-127">В приведенном ниже примере определяется метод из метода [**клеаревентлог**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) в [**Win32 \_ нтевентлогфиле**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="9f609-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="9f609-128">Этот квалификатор допустим только в том случае, если он используется с представлениями Union.</span><span class="sxs-lookup"><span data-stu-id="9f609-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="9f609-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**постжоинфилтер**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f609-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f609-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f609-130">Data type: **string**</span></span>

<span data-ttu-id="9f609-131">WQL-запрос для фильтрации экземпляров после их соединения в классе соединения.</span><span class="sxs-lookup"><span data-stu-id="9f609-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="9f609-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**пропертисаурцес**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f609-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f609-133">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="9f609-133">Data type: **string array**</span></span>

<span data-ttu-id="9f609-134">Исходные свойства, из которых свойство класса представления получает данные.</span><span class="sxs-lookup"><span data-stu-id="9f609-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="9f609-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Наборов**</span><span class="sxs-lookup"><span data-stu-id="9f609-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="9f609-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9f609-136">Data type: **boolean**</span></span>

<span data-ttu-id="9f609-137">Указывает, определяется ли класс объединения.</span><span class="sxs-lookup"><span data-stu-id="9f609-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="9f609-138">Представления Union содержат экземпляры, основанные на объединении исходных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="9f609-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="9f609-139">Например, вы можете объявить следующее:</span><span class="sxs-lookup"><span data-stu-id="9f609-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="9f609-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**виевсаурцес**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f609-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f609-141">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="9f609-141">Data type: **string array**</span></span>

<span data-ttu-id="9f609-142">Набор запросов язык запросов WMI (WQL), определяющих исходные экземпляры и свойства, используемые в определенном классе представления.</span><span class="sxs-lookup"><span data-stu-id="9f609-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="9f609-143">Важность соответствия всех квалификаторов массива важна.</span><span class="sxs-lookup"><span data-stu-id="9f609-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="9f609-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**виевспацес**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="9f609-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f609-145">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="9f609-145">Data type: **string array**</span></span>

<span data-ttu-id="9f609-146">Пространства имен, в которых находятся исходные экземпляры.</span><span class="sxs-lookup"><span data-stu-id="9f609-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f609-147">Требования</span><span class="sxs-lookup"><span data-stu-id="9f609-147">Requirements</span></span>



| <span data-ttu-id="9f609-148">Требование</span><span class="sxs-lookup"><span data-stu-id="9f609-148">Requirement</span></span> | <span data-ttu-id="9f609-149">Значение</span><span class="sxs-lookup"><span data-stu-id="9f609-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9f609-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f609-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9f609-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f609-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9f609-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f609-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9f609-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f609-153">Windows Server 2008</span></span><br/> |



 

