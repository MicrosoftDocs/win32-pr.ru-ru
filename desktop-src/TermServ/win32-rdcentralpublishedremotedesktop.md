---
title: Класс Win32_RDCentralPublishedRemoteDesktop
description: Рабочий стол, опубликованный на другом компьютере для удаленного использования через службы терминалов.
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDCentralPublishedRemoteDesktop службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDCentralPublishedRemoteDesktop, описание
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490101"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="2bffc-105">\_Класс Win32 рдцентралпублишедремотедесктоп</span><span class="sxs-lookup"><span data-stu-id="2bffc-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="2bffc-106">Рабочий стол, опубликованный на другом компьютере для удаленного использования через службы терминалов</span><span class="sxs-lookup"><span data-stu-id="2bffc-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="2bffc-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2bffc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bffc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2bffc-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="2bffc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="2bffc-109">Members</span></span>

<span data-ttu-id="2bffc-110">Класс **Win32 \_ рдцентралпублишедремотедесктоп** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2bffc-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="2bffc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2bffc-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bffc-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2bffc-112">Properties</span></span>

<span data-ttu-id="2bffc-113">Класс **Win32 \_ рдцентралпублишедремотедесктоп** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2bffc-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bffc-114">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="2bffc-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2bffc-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bffc-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-118">Псевдоним рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2bffc-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-119">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2bffc-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2bffc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2bffc-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-123">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="2bffc-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="2bffc-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bffc-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2bffc-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2bffc-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-128">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2bffc-128">Description of the object.</span></span>

<span data-ttu-id="2bffc-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bffc-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-130">**Папки**</span><span class="sxs-lookup"><span data-stu-id="2bffc-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-131">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2bffc-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2bffc-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-133">Список папок, в которых должен отображаться этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="2bffc-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-134">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="2bffc-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-135">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2bffc-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2bffc-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-137">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2bffc-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-138">Содержимое значка, соответствующего приложению.</span><span class="sxs-lookup"><span data-stu-id="2bffc-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2bffc-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-140">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2bffc-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2bffc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="2bffc-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-143">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="2bffc-143">The date the object was installed.</span></span> <span data-ttu-id="2bffc-144">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="2bffc-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2bffc-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bffc-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-146">**Name**</span><span class="sxs-lookup"><span data-stu-id="2bffc-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2bffc-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-149">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="2bffc-149">The name of the object.</span></span>

<span data-ttu-id="2bffc-150">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bffc-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-151">**публишингфарм**</span><span class="sxs-lookup"><span data-stu-id="2bffc-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2bffc-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-154">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bffc-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-155">Псевдоним фермы, в которой опубликован рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="2bffc-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-156">**рдпфилеконтентс**</span><span class="sxs-lookup"><span data-stu-id="2bffc-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2bffc-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-159">Содержимое RDP-файла, соответствующего рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="2bffc-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-160">**шовинпортал**</span><span class="sxs-lookup"><span data-stu-id="2bffc-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-161">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2bffc-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-162">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2bffc-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-163">**значение true** , если это приложение должно отображаться на веб-доступ TS; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2bffc-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2bffc-164">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2bffc-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bffc-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2bffc-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2bffc-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bffc-167">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="2bffc-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="2bffc-168">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2bffc-168">Current status of the object.</span></span> <span data-ttu-id="2bffc-169">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="2bffc-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2bffc-170">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="2bffc-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2bffc-171">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="2bffc-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2bffc-172">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="2bffc-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2bffc-173">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="2bffc-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2bffc-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2bffc-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="2bffc-175">("ОК")</span><span class="sxs-lookup"><span data-stu-id="2bffc-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-176">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="2bffc-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-177">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="2bffc-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-178">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="2bffc-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-179">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="2bffc-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-180">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="2bffc-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-181">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="2bffc-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2bffc-182">("Служба")</span><span class="sxs-lookup"><span data-stu-id="2bffc-182">("Service")</span></span>


<span data-ttu-id="2bffc-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2bffc-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2bffc-184">Требования</span><span class="sxs-lookup"><span data-stu-id="2bffc-184">Requirements</span></span>



| <span data-ttu-id="2bffc-185">Требование</span><span class="sxs-lookup"><span data-stu-id="2bffc-185">Requirement</span></span> | <span data-ttu-id="2bffc-186">Значение</span><span class="sxs-lookup"><span data-stu-id="2bffc-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bffc-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bffc-187">Minimum supported client</span></span><br/> | <span data-ttu-id="2bffc-188">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2bffc-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2bffc-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bffc-189">Minimum supported server</span></span><br/> | <span data-ttu-id="2bffc-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2bffc-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="2bffc-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2bffc-191">Namespace</span></span><br/>                | <span data-ttu-id="2bffc-192">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="2bffc-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2bffc-193">MOF</span><span class="sxs-lookup"><span data-stu-id="2bffc-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bffc-194"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bffc-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="2bffc-195">DLL</span><span class="sxs-lookup"><span data-stu-id="2bffc-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bffc-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bffc-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

