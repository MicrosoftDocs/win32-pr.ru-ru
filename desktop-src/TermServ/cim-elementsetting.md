---
title: Класс CIM_ElementSetting (службы удаленных рабочих столов)
description: Представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.
ms.assetid: b74c2fef-0f3a-46b9-9dd8-11016a8f7b57
ms.tgt_platform: multiple
keywords:
- Класс CIM_ElementSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса CIM_ElementSetting, описание
topic_type:
- apiref
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Caption
- CIM_ElementSetting.Description
- CIM_ElementSetting.InstallDate
- CIM_ElementSetting.Name
- CIM_ElementSetting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9aff40961ddc8fa07de6c49d6c95aefe3d005d6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135338"
---
# <a name="cim_elementsetting-class-remote-desktop-services"></a><span data-ttu-id="0171c-105">Класс CIM_ElementSetting (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="0171c-105">CIM_ElementSetting class (Remote Desktop Services)</span></span>

<span data-ttu-id="0171c-106">Представляет ассоциацию между управляемыми системными элементами и определенным для них классом параметров.</span><span class="sxs-lookup"><span data-stu-id="0171c-106">Represents the association between managed system elements and the setting class defined for them.</span></span>

<span data-ttu-id="0171c-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0171c-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0171c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0171c-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="0171c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0171c-109">Members</span></span>

<span data-ttu-id="0171c-110">Класс **CIM \_ елементсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0171c-110">The **CIM\_ElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0171c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0171c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0171c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0171c-112">Properties</span></span>

<span data-ttu-id="0171c-113">Класс **CIM \_ елементсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0171c-113">The **CIM\_ElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0171c-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0171c-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0171c-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0171c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0171c-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0171c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0171c-117">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0171c-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0171c-118">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="0171c-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0171c-119">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0171c-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0171c-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0171c-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0171c-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0171c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0171c-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0171c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0171c-123">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0171c-123">Description of the object.</span></span>

<span data-ttu-id="0171c-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0171c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0171c-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0171c-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0171c-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0171c-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0171c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0171c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0171c-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0171c-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0171c-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0171c-129">The date the object was installed.</span></span> <span data-ttu-id="0171c-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="0171c-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0171c-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0171c-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0171c-132">**Name**</span><span class="sxs-lookup"><span data-stu-id="0171c-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0171c-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0171c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0171c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0171c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0171c-135">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0171c-135">The name of the object.</span></span>

<span data-ttu-id="0171c-136">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0171c-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0171c-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0171c-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0171c-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0171c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0171c-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0171c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0171c-140">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0171c-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0171c-141">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0171c-141">Current status of the object.</span></span> <span data-ttu-id="0171c-142">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="0171c-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0171c-143">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="0171c-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0171c-144">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="0171c-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0171c-145">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="0171c-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0171c-146">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="0171c-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0171c-147">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0171c-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0171c-148">("ОК")</span><span class="sxs-lookup"><span data-stu-id="0171c-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-149">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="0171c-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-150">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="0171c-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-151">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0171c-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-152">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0171c-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-153">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0171c-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-154">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="0171c-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0171c-155">("Служба")</span><span class="sxs-lookup"><span data-stu-id="0171c-155">("Service")</span></span>


<span data-ttu-id="0171c-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0171c-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0171c-157">Требования</span><span class="sxs-lookup"><span data-stu-id="0171c-157">Requirements</span></span>



| <span data-ttu-id="0171c-158">Требование</span><span class="sxs-lookup"><span data-stu-id="0171c-158">Requirement</span></span> | <span data-ttu-id="0171c-159">Значение</span><span class="sxs-lookup"><span data-stu-id="0171c-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0171c-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0171c-160">Minimum supported client</span></span><br/> | <span data-ttu-id="0171c-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0171c-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0171c-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0171c-162">Minimum supported server</span></span><br/> | <span data-ttu-id="0171c-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0171c-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0171c-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0171c-164">Namespace</span></span><br/>                | <span data-ttu-id="0171c-165">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0171c-165">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0171c-166">MOF</span><span class="sxs-lookup"><span data-stu-id="0171c-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0171c-167"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0171c-167"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0171c-168">DLL</span><span class="sxs-lookup"><span data-stu-id="0171c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0171c-169"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0171c-169"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0171c-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0171c-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0171c-171">**\_МАНАЖЕДСИСТЕМЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="0171c-171">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

