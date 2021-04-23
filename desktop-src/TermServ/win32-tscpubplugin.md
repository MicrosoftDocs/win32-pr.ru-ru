---
title: Класс Win32_TSCPubPlugin
description: Представляет подключаемый модуль, настроенный для использования в службе управление подключениями к удаленным рабочим столам и приложениям RemoteApp.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSCPubPlugin службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSCPubPlugin, описание
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891817"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="46883-105">\_Класс Win32 тскпубплугин</span><span class="sxs-lookup"><span data-stu-id="46883-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="46883-106">Представляет подключаемый модуль, настроенный для использования в службе управление подключениями к удаленным рабочим столам и приложениям RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="46883-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="46883-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="46883-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46883-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46883-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="46883-109">Члены</span><span class="sxs-lookup"><span data-stu-id="46883-109">Members</span></span>

<span data-ttu-id="46883-110">Класс **Win32 \_ тскпубплугин** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="46883-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="46883-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="46883-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46883-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="46883-112">Properties</span></span>

<span data-ttu-id="46883-113">Класс **Win32 \_ тскпубплугин** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="46883-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46883-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="46883-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46883-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46883-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46883-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46883-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="46883-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="46883-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="46883-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="46883-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46883-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46883-120">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="46883-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46883-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46883-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46883-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46883-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46883-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46883-124">Идентификатор CLSID подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="46883-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="46883-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46883-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46883-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46883-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46883-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46883-128">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="46883-128">Description of the object.</span></span>

<span data-ttu-id="46883-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46883-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46883-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46883-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-131">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="46883-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46883-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46883-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46883-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="46883-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="46883-134">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="46883-134">The date the object was installed.</span></span> <span data-ttu-id="46883-135">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="46883-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="46883-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46883-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46883-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="46883-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46883-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46883-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46883-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46883-140">Указывает, включен ли подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="46883-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="46883-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="46883-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46883-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46883-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46883-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46883-144">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="46883-144">The name of the object.</span></span>

<span data-ttu-id="46883-145">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46883-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46883-146">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="46883-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46883-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46883-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46883-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46883-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46883-149">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="46883-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="46883-150">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="46883-150">Current status of the object.</span></span> <span data-ttu-id="46883-151">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="46883-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="46883-152">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="46883-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="46883-153">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="46883-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46883-154">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="46883-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46883-155">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="46883-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46883-156">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46883-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="46883-157">("ОК")</span><span class="sxs-lookup"><span data-stu-id="46883-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-158">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="46883-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-159">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="46883-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-160">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="46883-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-161">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="46883-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-162">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="46883-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-163">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="46883-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46883-164">("Служба")</span><span class="sxs-lookup"><span data-stu-id="46883-164">("Service")</span></span>


<span data-ttu-id="46883-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46883-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="46883-166">Требования</span><span class="sxs-lookup"><span data-stu-id="46883-166">Requirements</span></span>



| <span data-ttu-id="46883-167">Требование</span><span class="sxs-lookup"><span data-stu-id="46883-167">Requirement</span></span> | <span data-ttu-id="46883-168">Значение</span><span class="sxs-lookup"><span data-stu-id="46883-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46883-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46883-169">Minimum supported client</span></span><br/> | <span data-ttu-id="46883-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="46883-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="46883-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46883-171">Minimum supported server</span></span><br/> | <span data-ttu-id="46883-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46883-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="46883-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46883-173">Namespace</span></span><br/>                | <span data-ttu-id="46883-174">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="46883-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="46883-175">MOF</span><span class="sxs-lookup"><span data-stu-id="46883-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46883-176"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46883-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="46883-177">DLL</span><span class="sxs-lookup"><span data-stu-id="46883-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46883-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46883-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

