---
title: Класс CIM_ManagedSystemElement (службы удаленных рабочих столов)
description: Базовый класс для иерархии системных элементов.
ms.assetid: c71c0441-381f-4a46-864c-9206c43a27d0
ms.tgt_platform: multiple
keywords:
- Класс CIM_ManagedSystemElement службы удаленных рабочих столов
- Службы удаленных рабочих столов класса CIM_ManagedSystemElement, описание
topic_type:
- apiref
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b242369df24724fdcc31ce925a229dba5bb515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135335"
---
# <a name="cim_managedsystemelement-class-remote-desktop-services"></a><span data-ttu-id="28ebd-105">Класс CIM_ManagedSystemElement (службы удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="28ebd-105">CIM_ManagedSystemElement class (Remote Desktop Services)</span></span>

<span data-ttu-id="28ebd-106">Базовый класс для иерархии системных элементов.</span><span class="sxs-lookup"><span data-stu-id="28ebd-106">The base class for the system element hierarchy.</span></span>

<span data-ttu-id="28ebd-107">Любой различимый системный компонент является кандидатом для включения в этот класс.</span><span class="sxs-lookup"><span data-stu-id="28ebd-107">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="28ebd-108">Примеры включают в себя программные компоненты, такие как файлы; устройства, такие как дисковые накопители и контроллеры; и физические компоненты, такие как микросхемы и карты</span><span class="sxs-lookup"><span data-stu-id="28ebd-108">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards</span></span>

<span data-ttu-id="28ebd-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="28ebd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ebd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28ebd-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="28ebd-111">Члены</span><span class="sxs-lookup"><span data-stu-id="28ebd-111">Members</span></span>

<span data-ttu-id="28ebd-112">Класс **CIM \_ манажедсистемелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="28ebd-112">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="28ebd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="28ebd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="28ebd-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="28ebd-114">Properties</span></span>

<span data-ttu-id="28ebd-115">Класс **CIM \_ манажедсистемелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="28ebd-115">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="28ebd-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="28ebd-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28ebd-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="28ebd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28ebd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="28ebd-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="28ebd-120">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="28ebd-120">Short description (one-line string) of the object.</span></span>

</dd> <dt>

<span data-ttu-id="28ebd-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="28ebd-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28ebd-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="28ebd-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28ebd-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28ebd-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="28ebd-124">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="28ebd-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="28ebd-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28ebd-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="28ebd-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28ebd-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="28ebd-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="28ebd-129">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="28ebd-129">The date the object was installed.</span></span> <span data-ttu-id="28ebd-130">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="28ebd-130">A lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="28ebd-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="28ebd-131">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28ebd-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="28ebd-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28ebd-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="28ebd-134">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="28ebd-134">The name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="28ebd-135">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="28ebd-135">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="28ebd-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="28ebd-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="28ebd-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="28ebd-138">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="28ebd-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="28ebd-139">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="28ebd-139">Current status of the object.</span></span> <span data-ttu-id="28ebd-140">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="28ebd-140">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="28ebd-141">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="28ebd-141">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="28ebd-142">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="28ebd-142">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="28ebd-143">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="28ebd-143">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="28ebd-144">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="28ebd-144">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<dt>



 <span data-ttu-id="28ebd-145">("ОК")</span><span class="sxs-lookup"><span data-stu-id="28ebd-145">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-146">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="28ebd-146">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-147">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="28ebd-147">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-148">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="28ebd-148">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-149">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="28ebd-149">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-150">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="28ebd-150">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-151">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="28ebd-151">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="28ebd-152">("Служба")</span><span class="sxs-lookup"><span data-stu-id="28ebd-152">("Service")</span></span>


<span data-ttu-id="28ebd-153"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="28ebd-153"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="28ebd-154">Требования</span><span class="sxs-lookup"><span data-stu-id="28ebd-154">Requirements</span></span>



| <span data-ttu-id="28ebd-155">Требование</span><span class="sxs-lookup"><span data-stu-id="28ebd-155">Requirement</span></span> | <span data-ttu-id="28ebd-156">Значение</span><span class="sxs-lookup"><span data-stu-id="28ebd-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28ebd-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28ebd-157">Minimum supported client</span></span><br/> | <span data-ttu-id="28ebd-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28ebd-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="28ebd-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28ebd-159">Minimum supported server</span></span><br/> | <span data-ttu-id="28ebd-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28ebd-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="28ebd-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="28ebd-161">Namespace</span></span><br/>                | <span data-ttu-id="28ebd-162">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="28ebd-162">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="28ebd-163">MOF</span><span class="sxs-lookup"><span data-stu-id="28ebd-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28ebd-164"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28ebd-164"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="28ebd-165">DLL</span><span class="sxs-lookup"><span data-stu-id="28ebd-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28ebd-166"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28ebd-166"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



 

