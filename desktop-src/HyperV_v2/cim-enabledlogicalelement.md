---
description: Представляет логический элемент, который может быть включен и отключен.
ms.assetid: 52eed77e-f3f1-4489-8eff-a8ebebd5e1a8
title: Класс CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement
- CIM_EnabledLogicalElement.EnabledState
- CIM_EnabledLogicalElement.OtherEnabledState
- CIM_EnabledLogicalElement.RequestedState
- CIM_EnabledLogicalElement.EnabledDefault
- CIM_EnabledLogicalElement.TimeOfLastStateChange
- CIM_EnabledLogicalElement.AvailableRequestedStates
- CIM_EnabledLogicalElement.TransitioningToState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e2d7043653b219bc0d54ac7bee3393275dab673
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683557"
---
# <a name="cim_enabledlogicalelement-class"></a><span data-ttu-id="5a212-103">\_Класс CIM енабледлогикалелемент</span><span class="sxs-lookup"><span data-stu-id="5a212-103">CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="5a212-104">Представляет логический элемент, который может быть включен и отключен.</span><span class="sxs-lookup"><span data-stu-id="5a212-104">Represents a logical element that can be enabled and disabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a212-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a212-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_EnabledLogicalElement : CIM_LogicalElement
{
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
};
```

## <a name="members"></a><span data-ttu-id="5a212-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5a212-106">Members</span></span>

<span data-ttu-id="5a212-107">Класс **CIM \_ енабледлогикалелемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5a212-107">The **CIM\_EnabledLogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="5a212-108">Методы</span><span class="sxs-lookup"><span data-stu-id="5a212-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a212-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a212-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a212-110">Методы</span><span class="sxs-lookup"><span data-stu-id="5a212-110">Methods</span></span>

<span data-ttu-id="5a212-111">Класс **CIM \_ енабледлогикалелемент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5a212-111">The **CIM\_EnabledLogicalElement** class has these methods.</span></span>



| <span data-ttu-id="5a212-112">Метод</span><span class="sxs-lookup"><span data-stu-id="5a212-112">Method</span></span>                                                                     | <span data-ttu-id="5a212-113">Описание</span><span class="sxs-lookup"><span data-stu-id="5a212-113">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a212-114">**Равен**</span><span class="sxs-lookup"><span data-stu-id="5a212-114">**RequestStateChange**</span></span>](cim-enabledlogicalelement-requeststatechange.md) | <span data-ttu-id="5a212-115">Запрашивает изменение состояния элемента на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="5a212-115">Requests that the state of the element be changed to the specified value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5a212-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a212-116">Properties</span></span>

<span data-ttu-id="5a212-117">Класс **CIM \_ енабледлогикалелемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5a212-117">The **CIM\_EnabledLogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a212-118">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="5a212-118">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-119">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5a212-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5a212-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a212-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a212-121">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелемент**.**RequestStateChange**","[**CIM \_ енабледлогикалелементкапабилитиес**](cim-enabledlogicalelementcapabilities.md).**Рекуестедстатессуппортед**")</span><span class="sxs-lookup"><span data-stu-id="5a212-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "[**CIM\_EnabledLogicalElementCapabilities**](cim-enabledlogicalelementcapabilities.md).**RequestedStatesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="5a212-122">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="5a212-122">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<span data-ttu-id="5a212-123">Указанные значения должны быть подмножеством значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="5a212-123">The listed values must be a subset of the values that are contained in the **RequestedStatesSupported** property of the associated **CIM\_EnabledLogicalElementCapabilities** instance.</span></span> <span data-ttu-id="5a212-124">Это свойство имеет **значение NULL** , если реализация не может определить набор возможных значений для текущего состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="5a212-124">This property is **NULL** if the implementation cannot determine the set of possible values for the current state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a212-125">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="5a212-125">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a212-126">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="5a212-126">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="5a212-127">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="5a212-127">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="5a212-128">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="5a212-128">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="5a212-129">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="5a212-129">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="5a212-130">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="5a212-130">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="5a212-131">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="5a212-131">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="5a212-132">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="5a212-132">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="5a212-133">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="5a212-133">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5a212-134">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5a212-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a212-135">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="5a212-135">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-136">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a212-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a212-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5a212-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5a212-138">Указывает конфигурацию по умолчанию или запуск администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="5a212-138">Indicates an administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5a212-139">Значение по умолчанию **включено** (2).</span><span class="sxs-lookup"><span data-stu-id="5a212-139">The default value **Enabled** (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a212-140">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="5a212-140">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a212-141">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="5a212-141">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5a212-142">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="5a212-142">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="5a212-143">**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="5a212-143">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Default"></span><span id="no_default"></span><span id="NO_DEFAULT"></span>

<span data-ttu-id="5a212-144">**Нет значения по умолчанию** (7)</span><span class="sxs-lookup"><span data-stu-id="5a212-144">**No Default** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="5a212-145">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="5a212-145">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5a212-146">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5a212-146">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5a212-147">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5a212-147">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a212-148">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5a212-148">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a212-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a212-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a212-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a212-151">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелемент**.**Осеренабледстате**")</span><span class="sxs-lookup"><span data-stu-id="5a212-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**OtherEnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="5a212-152">Указывает включенное состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="5a212-152">Indicates the enabled state of an element.</span></span> <span data-ttu-id="5a212-153">Возможные значения включают переходы между состояниями.</span><span class="sxs-lookup"><span data-stu-id="5a212-153">Possible values include the transitions between states.</span></span> <span data-ttu-id="5a212-154">Например, **Завершение работы** (4) и **Запуск** (10) являются временными состояниями между **включенным** и **отключенным**.</span><span class="sxs-lookup"><span data-stu-id="5a212-154">For example, **Shutting Down** (4) and **Starting** (10) are transient states between **Enabled** and **Disabled**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a212-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5a212-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5a212-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5a212-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a212-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="5a212-157"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-158">Элемент или может выполнять команды, обрабатывает все команды в очереди и помещает новые запросы в очередь.</span><span class="sxs-lookup"><span data-stu-id="5a212-158">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a212-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="5a212-159"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-160">элемент не будет выполнять команды и удалит все новые запросы.</span><span class="sxs-lookup"><span data-stu-id="5a212-160">the element will not execute commands and will drop any new requests.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="5a212-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="5a212-161"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-162">Элемент находится в процессе перехода в отключенное состояние.</span><span class="sxs-lookup"><span data-stu-id="5a212-162">The element is in the process of going to a Disabled state.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5a212-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="5a212-163"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-164">Элемент не поддерживает включение или отключение.</span><span class="sxs-lookup"><span data-stu-id="5a212-164">The element does not support being enabled or disabled.</span></span>

</dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="5a212-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)</span><span class="sxs-lookup"><span data-stu-id="5a212-165"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-166">Элемент может выполнять команды, а все новые запросы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="5a212-166">The element might be completing commands, and will drop any new requests.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5a212-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (7)</span><span class="sxs-lookup"><span data-stu-id="5a212-167"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-168">Элемент находится в состоянии теста.</span><span class="sxs-lookup"><span data-stu-id="5a212-168">The element is in a test state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="5a212-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="5a212-169"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-170">Элемент может выполнять команды, но будет ставить в очередь новые запросы.</span><span class="sxs-lookup"><span data-stu-id="5a212-170">The element might be completing commands, but will queue any new requests.</span></span>

</dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="5a212-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="5a212-171"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-172">, Что элемент включен, но находится в ограниченном режиме.</span><span class="sxs-lookup"><span data-stu-id="5a212-172">That the element is enabled but in a restricted mode.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5a212-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (10)</span><span class="sxs-lookup"><span data-stu-id="5a212-173"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-174">Элемент находится в процессе перехода в состояние Enabled.</span><span class="sxs-lookup"><span data-stu-id="5a212-174">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="5a212-175">Новые запросы помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="5a212-175">New requests are queued.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5a212-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (11.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5a212-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (11..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5a212-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5a212-177"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a212-178">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="5a212-178">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5a212-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a212-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a212-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a212-181">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелемент**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="5a212-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="5a212-182">Описывает состояние элемента, если значение свойства **EnabledState** равно **other**.</span><span class="sxs-lookup"><span data-stu-id="5a212-182">Describes the state of the element when the value of the **EnabledState** property is **Other**.</span></span> <span data-ttu-id="5a212-183">Это свойство должно иметь значение **null** , если **EnabledState** не является **другим**.</span><span class="sxs-lookup"><span data-stu-id="5a212-183">This property must be set to **NULL** when **EnabledState** is not **Other**.</span></span>

</dd> <dt>

<span data-ttu-id="5a212-184">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5a212-184">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-185">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a212-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a212-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a212-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a212-187">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелемент**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="5a212-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="5a212-188">Указывает Последнее запрошенное состояние для элемента.</span><span class="sxs-lookup"><span data-stu-id="5a212-188">Indicates the last requested state for the element.</span></span> <span data-ttu-id="5a212-189">Текущее состояние указывается свойством **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5a212-189">The current state is indicated by the **EnabledState** property.</span></span> <span data-ttu-id="5a212-190">Это свойство позволяет сравнивать последние запрошенные и текущие состояния.</span><span class="sxs-lookup"><span data-stu-id="5a212-190">This property enables you to compare the last requested and current states.</span></span>

> [!Note]  
> <span data-ttu-id="5a212-191">Если значение свойства **EnabledState** **неприменимо**, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="5a212-191">When the value of the **EnabledState** property is **Not Applicable**, this property has no meaning.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a212-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5a212-192"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-193">Последнее запрошенное состояние элемента неизвестно.</span><span class="sxs-lookup"><span data-stu-id="5a212-193">The last requested state for the element is unknown.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a212-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="5a212-194"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a212-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="5a212-195"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-196">Запрашивает немедленное отключение элемента, так что он не будет выполнять или принимать команды или обрабатывать запросы.</span><span class="sxs-lookup"><span data-stu-id="5a212-196">Requests an immediate disabling of the element, such that it will not execute or accept any commands or processing requests.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="5a212-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="5a212-197"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-198">Запрашивает переход в отключенное состояние и может включать удаление электропитания, чтобы полностью стереть любое существующее состояние.</span><span class="sxs-lookup"><span data-stu-id="5a212-198">Requests an orderly transition to the Disabled state, and might involve removing power, to completely erase any existing state.</span></span>

</dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="5a212-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Без изменений** (5)</span><span class="sxs-lookup"><span data-stu-id="5a212-199"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-200">Не рекомендуется использовать вместо указания последнего запрошенного состояния "неизвестно" (0).</span><span class="sxs-lookup"><span data-stu-id="5a212-200">Deprecated in lieu of indicating the last requested state is "Unknown" (0).</span></span> <span data-ttu-id="5a212-201">Если последнее запрошенное или требуемое состояние неизвестно, то параметр **RequestedState** должен иметь значение "Unknown" (0), но может иметь значение "без изменений" (5).</span><span class="sxs-lookup"><span data-stu-id="5a212-201">If the last requested or desired state is unknown, **RequestedState** should have the value "Unknown" (0), but may have the value "No Change" (5).</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="5a212-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="5a212-202"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-203">Элемент получил запрос на переход к включенному, но не в сети **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5a212-203">The element has been requested to transition to the Enabled but Offline **EnabledState**.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="5a212-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="5a212-204"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="5a212-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)</span><span class="sxs-lookup"><span data-stu-id="5a212-205"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="5a212-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="5a212-206"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="5a212-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="5a212-207"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-208">Обозначает выполнение "выключения" и переход в состояние "включено".</span><span class="sxs-lookup"><span data-stu-id="5a212-208">Refers to doing a "Shut Down" and then moving to an "Enabled" state.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="5a212-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="5a212-209"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="5a212-210">Указывает, что элемент является первым "отключенным", а затем "Enabled".</span><span class="sxs-lookup"><span data-stu-id="5a212-210">Indicates that the element is first "Disabled" and then "Enabled".</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5a212-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (12)</span><span class="sxs-lookup"><span data-stu-id="5a212-211"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5a212-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5a212-212"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="5a212-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5a212-213"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5a212-214">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="5a212-214">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-215">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5a212-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5a212-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a212-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a212-217">Указывает, когда состояние последнего изменения элемента.</span><span class="sxs-lookup"><span data-stu-id="5a212-217">Indicates when the element last changed state.</span></span> <span data-ttu-id="5a212-218">Если состояние элемента не изменилось и заполнено это свойство, то для него должно быть задано нулевое значение интервала.</span><span class="sxs-lookup"><span data-stu-id="5a212-218">If the state of the element has not changed and this property is populated, then it must be set to a zero interval value.</span></span> <span data-ttu-id="5a212-219">Если изменение состояния было запрошено, но было отклонено или еще не обработано, свойство не должно обновляться.</span><span class="sxs-lookup"><span data-stu-id="5a212-219">If a state change was requested, but was rejected or is not yet processed, the property must not be updated.</span></span>

</dd> <dt>

<span data-ttu-id="5a212-220">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="5a212-220">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a212-221">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5a212-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5a212-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a212-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a212-223">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ енабледлогикалелемент**.**RequestStateChange**","**CIM \_ енабледлогикалелемент**.**RequestedState**","**CIM \_ енабледлогикалелемент**.**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="5a212-223">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElement**.**RequestStateChange**", "**CIM\_EnabledLogicalElement**.**RequestedState**", "**CIM\_EnabledLogicalElement**.**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="5a212-224">Указывает целевое состояние, в которое изменяется экземпляр.</span><span class="sxs-lookup"><span data-stu-id="5a212-224">Indicates the target state to which the instance is changing.</span></span>

<span data-ttu-id="5a212-225">Значение **без изменений** означает, что переход не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a212-225">A value of **No Change** indicates that no transition is in progress.</span></span> <span data-ttu-id="5a212-226">Значение **неприменимо** указывает, что реализация не сообщает о текущих переходах.</span><span class="sxs-lookup"><span data-stu-id="5a212-226">A value of **Not Applicable** indicates that the implementation does not report ongoing transitions.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5a212-227">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="5a212-227">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5a212-228">**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="5a212-228">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5a212-229">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="5a212-229">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="5a212-230">**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="5a212-230">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="5a212-231">**Без изменений** (5)</span><span class="sxs-lookup"><span data-stu-id="5a212-231">**No Change** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="5a212-232">**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="5a212-232">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="5a212-233">**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="5a212-233">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="5a212-234">**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="5a212-234">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="5a212-235">**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="5a212-235">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="5a212-236">**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="5a212-236">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="5a212-237">**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="5a212-237">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5a212-238">**Неприменимо** (12)</span><span class="sxs-lookup"><span data-stu-id="5a212-238">**Not Applicable** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5a212-239">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="5a212-239">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="5a212-240"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5a212-240"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5a212-241">Требования</span><span class="sxs-lookup"><span data-stu-id="5a212-241">Requirements</span></span>



| <span data-ttu-id="5a212-242">Требование</span><span class="sxs-lookup"><span data-stu-id="5a212-242">Requirement</span></span> | <span data-ttu-id="5a212-243">Значение</span><span class="sxs-lookup"><span data-stu-id="5a212-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a212-244">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a212-244">Minimum supported client</span></span><br/> | <span data-ttu-id="5a212-245">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5a212-245">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5a212-246">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a212-246">Minimum supported server</span></span><br/> | <span data-ttu-id="5a212-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a212-247">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5a212-248">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5a212-248">Namespace</span></span><br/>                | <span data-ttu-id="5a212-249">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5a212-249">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5a212-250">MOF</span><span class="sxs-lookup"><span data-stu-id="5a212-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a212-251"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a212-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a212-252">DLL</span><span class="sxs-lookup"><span data-stu-id="5a212-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a212-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5a212-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5a212-254">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a212-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a212-255">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="5a212-255">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

