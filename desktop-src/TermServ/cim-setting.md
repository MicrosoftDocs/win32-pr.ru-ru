---
title: Класс CIM_Setting (службы удаленных рабочих столов)
description: Представляет связанные с конфигурацией и операционные параметры для одного или нескольких управляемых системных элементов.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- Класс CIM_Setting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса CIM_Setting, описание
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d3a9517df9af92f428000ed064b2bb88b348a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672522"
---
# <a name="cim_setting-class-remote-desktop-services"></a><span data-ttu-id="95aca-105">Класс CIM_Setting (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="95aca-105">CIM_Setting class (Remote Desktop Services)</span></span>

<span data-ttu-id="95aca-106">Представляет связанные с конфигурацией и операционные параметры для одного или нескольких управляемых системных элементов.</span><span class="sxs-lookup"><span data-stu-id="95aca-106">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

<span data-ttu-id="95aca-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="95aca-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="95aca-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95aca-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="95aca-109">Члены</span><span class="sxs-lookup"><span data-stu-id="95aca-109">Members</span></span>

<span data-ttu-id="95aca-110">Класс **\_ параметров CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="95aca-110">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="95aca-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="95aca-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95aca-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="95aca-112">Properties</span></span>

<span data-ttu-id="95aca-113">Класс **\_ параметров CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="95aca-113">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95aca-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="95aca-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95aca-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95aca-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95aca-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95aca-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95aca-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="95aca-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="95aca-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="95aca-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="95aca-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95aca-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95aca-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95aca-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95aca-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95aca-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95aca-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95aca-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95aca-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="95aca-123">Description of the object.</span></span>

<span data-ttu-id="95aca-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95aca-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95aca-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="95aca-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95aca-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95aca-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95aca-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95aca-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95aca-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="95aca-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="95aca-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="95aca-129">The date the object was installed.</span></span> <span data-ttu-id="95aca-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="95aca-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="95aca-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95aca-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95aca-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="95aca-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95aca-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95aca-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95aca-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95aca-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95aca-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="95aca-135">The name of the object.</span></span>

<span data-ttu-id="95aca-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95aca-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95aca-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="95aca-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95aca-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95aca-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95aca-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95aca-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95aca-140">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="95aca-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="95aca-141">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="95aca-141">Current status of the object.</span></span> <span data-ttu-id="95aca-142">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="95aca-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="95aca-143">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="95aca-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="95aca-144">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="95aca-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="95aca-145">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="95aca-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="95aca-146">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="95aca-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="95aca-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95aca-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="95aca-148">("ОК")</span><span class="sxs-lookup"><span data-stu-id="95aca-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-149">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="95aca-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-150">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="95aca-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-151">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="95aca-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-152">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="95aca-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-153">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="95aca-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-154">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="95aca-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="95aca-155">("Служба")</span><span class="sxs-lookup"><span data-stu-id="95aca-155">("Service")</span></span>


<span data-ttu-id="95aca-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="95aca-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="95aca-157">Требования</span><span class="sxs-lookup"><span data-stu-id="95aca-157">Requirements</span></span>



| <span data-ttu-id="95aca-158">Требование</span><span class="sxs-lookup"><span data-stu-id="95aca-158">Requirement</span></span> | <span data-ttu-id="95aca-159">Значение</span><span class="sxs-lookup"><span data-stu-id="95aca-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95aca-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95aca-160">Minimum supported client</span></span><br/> | <span data-ttu-id="95aca-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95aca-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95aca-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95aca-162">Minimum supported server</span></span><br/> | <span data-ttu-id="95aca-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95aca-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95aca-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95aca-164">Namespace</span></span><br/>                | <span data-ttu-id="95aca-165">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="95aca-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="95aca-166">MOF</span><span class="sxs-lookup"><span data-stu-id="95aca-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95aca-167"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95aca-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="95aca-168">DLL</span><span class="sxs-lookup"><span data-stu-id="95aca-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95aca-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95aca-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95aca-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95aca-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95aca-171">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="95aca-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

