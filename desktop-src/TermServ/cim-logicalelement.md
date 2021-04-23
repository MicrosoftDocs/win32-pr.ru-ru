---
title: Класс CIM_LogicalElement (службы удаленных рабочих столов)
description: Базовый класс для всех системных компонентов, представляющих абстрактные системные компоненты, такие как профили, процессы или возможности системы, в форме логических устройств.
ms.assetid: 21e4a2ba-7bc5-4e33-a888-198299137da6
ms.tgt_platform: multiple
keywords:
- Класс CIM_LogicalElement службы удаленных рабочих столов
- Службы удаленных рабочих столов класса CIM_LogicalElement, описание
topic_type:
- apiref
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f7e58fe64f3b9dbb76a11d308aadbe6ce50331f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414961"
---
# <a name="cim_logicalelement-class-remote-desktop-services"></a><span data-ttu-id="1bd4a-105">Класс CIM_LogicalElement (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="1bd4a-105">CIM_LogicalElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="1bd4a-106">Базовый класс для всех системных компонентов, представляющих абстрактные системные компоненты, такие как профили, процессы или возможности системы, в форме логических устройств.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-106">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

<span data-ttu-id="1bd4a-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd4a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bd4a-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="1bd4a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1bd4a-109">Members</span></span>

<span data-ttu-id="1bd4a-110">Класс **CIM \_ логикалелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1bd4a-110">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="1bd4a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1bd4a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bd4a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1bd4a-112">Properties</span></span>

<span data-ttu-id="1bd4a-113">Класс **CIM \_ логикалелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-113">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1bd4a-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd4a-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1bd4a-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1bd4a-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1bd4a-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1bd4a-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1bd4a-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bd4a-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd4a-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1bd4a-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd4a-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-123">Description of the object.</span></span>

<span data-ttu-id="1bd4a-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1bd4a-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bd4a-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd4a-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1bd4a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="1bd4a-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1bd4a-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-129">The date the object was installed.</span></span> <span data-ttu-id="1bd4a-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1bd4a-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1bd4a-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bd4a-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd4a-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1bd4a-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1bd4a-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-135">The name of the object.</span></span>

<span data-ttu-id="1bd4a-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1bd4a-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bd4a-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bd4a-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1bd4a-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bd4a-140">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="1bd4a-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1bd4a-141">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-141">Current status of the object.</span></span> <span data-ttu-id="1bd4a-142">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1bd4a-143">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="1bd4a-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1bd4a-144">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="1bd4a-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1bd4a-145">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1bd4a-146">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1bd4a-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1bd4a-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1bd4a-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1bd4a-148">("ОК")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-149">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-150">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-151">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-152">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-153">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-154">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1bd4a-155">("Служба")</span><span class="sxs-lookup"><span data-stu-id="1bd4a-155">("Service")</span></span>


<span data-ttu-id="1bd4a-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1bd4a-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1bd4a-157">Требования</span><span class="sxs-lookup"><span data-stu-id="1bd4a-157">Requirements</span></span>



| <span data-ttu-id="1bd4a-158">Требование</span><span class="sxs-lookup"><span data-stu-id="1bd4a-158">Requirement</span></span> | <span data-ttu-id="1bd4a-159">Значение</span><span class="sxs-lookup"><span data-stu-id="1bd4a-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd4a-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bd4a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1bd4a-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bd4a-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1bd4a-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bd4a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1bd4a-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bd4a-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1bd4a-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1bd4a-164">Namespace</span></span><br/>                | <span data-ttu-id="1bd4a-165">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="1bd4a-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1bd4a-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1bd4a-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bd4a-167"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bd4a-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bd4a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="1bd4a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bd4a-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bd4a-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bd4a-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bd4a-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd4a-171">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="1bd4a-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

