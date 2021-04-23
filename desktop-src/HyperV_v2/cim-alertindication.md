---
description: Конкретный суперкласс для уведомлений об оповещениях CIM.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: Класс CIM_AlertIndication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682424"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="48851-103">\_Класс CIM алертиндикатион</span><span class="sxs-lookup"><span data-stu-id="48851-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="48851-104">Конкретный суперкласс для уведомлений об оповещениях CIM.</span><span class="sxs-lookup"><span data-stu-id="48851-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="48851-105">**Модель CIM \_ Алертиндикатион** — это специализированный тип **класса \_ индикации CIM** , который содержит сведения о серьезности, причине, рекомендуемых действиях и других данных для реального мира.</span><span class="sxs-lookup"><span data-stu-id="48851-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="48851-106">Это событие и его данные могут быть не смоделированы в иерархии классов CIM.</span><span class="sxs-lookup"><span data-stu-id="48851-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="48851-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48851-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="48851-108">Члены</span><span class="sxs-lookup"><span data-stu-id="48851-108">Members</span></span>

<span data-ttu-id="48851-109">Класс **CIM \_ алертиндикатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="48851-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="48851-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="48851-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48851-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="48851-111">Properties</span></span>

<span data-ttu-id="48851-112">Класс **CIM \_ алертиндикатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="48851-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48851-113">**алертинжелементформат**</span><span class="sxs-lookup"><span data-stu-id="48851-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48851-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48851-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-116">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Алертингманажеделемент**","**CIM \_ алертиндикатион**.**Осералертинжелементформат**")</span><span class="sxs-lookup"><span data-stu-id="48851-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-117">Формат свойства **алертингманажеделемент** .</span><span class="sxs-lookup"><span data-stu-id="48851-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48851-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="48851-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48851-119">Неизвестный или неосмысленный формат, интерпретируемый клиентским приложением CIM.</span><span class="sxs-lookup"><span data-stu-id="48851-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48851-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="48851-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48851-121">Формат определяется значением свойства Осералертинжелементформат.</span><span class="sxs-lookup"><span data-stu-id="48851-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="48851-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Цимобжектпас** (2)</span><span class="sxs-lookup"><span data-stu-id="48851-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48851-123">Формат — это Цимобжектпас, указывающий экземпляр в схеме CIM.</span><span class="sxs-lookup"><span data-stu-id="48851-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48851-124">**алертингманажеделемент**</span><span class="sxs-lookup"><span data-stu-id="48851-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-127">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Алертинжелементформат**")</span><span class="sxs-lookup"><span data-stu-id="48851-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-128">Идентифицирующие сведения сущности (IE, экземпляр), для которой создается это обозначение.</span><span class="sxs-lookup"><span data-stu-id="48851-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="48851-129">Свойство содержит путь к экземпляру, закодированный как строковый параметр, если экземпляр моделируется в схеме CIM.</span><span class="sxs-lookup"><span data-stu-id="48851-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="48851-130">Если не является экземпляром CIM, свойство содержит некоторую идентифицирующую строку, которая именует сущность, для которой создается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="48851-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="48851-131">Путь или идентифицирующая строка форматируются в соответствии со свойством Алертинжелементформат.</span><span class="sxs-lookup"><span data-stu-id="48851-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="48851-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="48851-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-133">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48851-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48851-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-135">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Тип события ")</span><span class="sxs-lookup"><span data-stu-id="48851-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="48851-136">Основная классификация индикации.</span><span class="sxs-lookup"><span data-stu-id="48851-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48851-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="48851-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48851-138">\- Иной.</span><span class="sxs-lookup"><span data-stu-id="48851-138">\- Other.</span></span> <span data-ttu-id="48851-139">Свойство Осералерттипе для индикации передает свою классификацию.</span><span class="sxs-lookup"><span data-stu-id="48851-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="48851-140">Использование "Other" в перечислении является стандартным соглашением CIM.</span><span class="sxs-lookup"><span data-stu-id="48851-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="48851-141">Это означает, что текущая индикация не помещается в категории, описанные в этом перечислении.</span><span class="sxs-lookup"><span data-stu-id="48851-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="48851-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Оповещение о связи** (2)</span><span class="sxs-lookup"><span data-stu-id="48851-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48851-143">Указание этого типа, как основное, связано с процедурами и (или) процессами, необходимыми для передачи информации из одной точки в другую.</span><span class="sxs-lookup"><span data-stu-id="48851-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="48851-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Предупреждение качества обслуживания** (3)</span><span class="sxs-lookup"><span data-stu-id="48851-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48851-145">Указание этого типа, как основное, связано с ухудшением или ошибками в производительности или функции сущности.</span><span class="sxs-lookup"><span data-stu-id="48851-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="48851-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Ошибка обработки** (4)</span><span class="sxs-lookup"><span data-stu-id="48851-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="48851-147">Указывает, что этот тип является основным, связанным с программным обеспечением или ошибкой обработки.</span><span class="sxs-lookup"><span data-stu-id="48851-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="48851-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Оповещение устройства** (5)</span><span class="sxs-lookup"><span data-stu-id="48851-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="48851-149">Указывает, что этот тип является основным, связанным с оборудованием или аппаратным сбоем.</span><span class="sxs-lookup"><span data-stu-id="48851-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="48851-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Оповещение о окружающей среде** (6)</span><span class="sxs-lookup"><span data-stu-id="48851-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="48851-151">Оповещение о рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="48851-151">Environmental Alert.</span></span> <span data-ttu-id="48851-152">Индикатор этого типа связан с условием, связанным с корпусом, в котором находится оборудование, или другими аспектами среды.</span><span class="sxs-lookup"><span data-stu-id="48851-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="48851-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Изменение модели** (7)</span><span class="sxs-lookup"><span data-stu-id="48851-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="48851-154">Указание устраняет изменения в информационной модели.</span><span class="sxs-lookup"><span data-stu-id="48851-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="48851-155">Например, он может внедрить обозначение жизненного цикла, чтобы передать оповещение об изменении конкретной модели.</span><span class="sxs-lookup"><span data-stu-id="48851-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="48851-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Оповещение системы безопасности** (8)</span><span class="sxs-lookup"><span data-stu-id="48851-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="48851-157">.</span><span class="sxs-lookup"><span data-stu-id="48851-157">.</span></span> <span data-ttu-id="48851-158">Указывает, что этот тип связан.</span><span class="sxs-lookup"><span data-stu-id="48851-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48851-159">**Описание**</span><span class="sxs-lookup"><span data-stu-id="48851-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-162">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Дополнительный текст ")</span><span class="sxs-lookup"><span data-stu-id="48851-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="48851-163">Краткое описание индикации.</span><span class="sxs-lookup"><span data-stu-id="48851-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="48851-164">**EventID**</span><span class="sxs-lookup"><span data-stu-id="48851-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-167">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Пробаблекаусе**")</span><span class="sxs-lookup"><span data-stu-id="48851-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-168">Конкретное значение инструментирования или поставщика, описывающее базовое реальное событие, представленное указанием.</span><span class="sxs-lookup"><span data-stu-id="48851-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="48851-169">Для представления одного и того же события в создаваемой сущности рассматриваются события с одинаковыми значениями **EventID** , отличными от NULL.</span><span class="sxs-lookup"><span data-stu-id="48851-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="48851-170">Сравнение двух значений **EventID** определено только для оповещений с одинаковыми значениями, отличными от NULL, для свойств **системкреатекласснаме**, **SystemName** и **providerName** .</span><span class="sxs-lookup"><span data-stu-id="48851-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="48851-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="48851-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-172">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48851-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48851-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-174">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Пробаблекаусе**")</span><span class="sxs-lookup"><span data-stu-id="48851-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-175">Дата и время, которые указывают, когда произошло первое обнаружение базового события.</span><span class="sxs-lookup"><span data-stu-id="48851-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="48851-176">Если эти значения указаны и создание сущности не может предоставить эти сведения, это свойство должно иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="48851-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="48851-177">Это значение основано на соотношении локальной даты и времени объекта **CIM \_ манажесистемелемент** , который создал указание.</span><span class="sxs-lookup"><span data-stu-id="48851-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="48851-178">**Message**</span><span class="sxs-lookup"><span data-stu-id="48851-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-181">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**MessageID**","**CIM \_ алертиндикатион**.**Мессажеаргументс**")</span><span class="sxs-lookup"><span data-stu-id="48851-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-182">Форматированное сообщение для индикации предупреждения.</span><span class="sxs-lookup"><span data-stu-id="48851-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="48851-183">Это сообщение форматируется путем объединения одного или нескольких динамических элементов, указанных в свойстве **мессажеаргументс** , и статических элементов, которые уникально идентифицируются свойством **MessageId** .</span><span class="sxs-lookup"><span data-stu-id="48851-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="48851-184">**мессажеаргументс**</span><span class="sxs-lookup"><span data-stu-id="48851-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-185">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="48851-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48851-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-187">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Message**","**CIM \_ алертиндикатион**.**MessageID**")</span><span class="sxs-lookup"><span data-stu-id="48851-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-188">Массив, содержащий динамическое содержимое сообщения для индикации предупреждения.</span><span class="sxs-lookup"><span data-stu-id="48851-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="48851-189">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="48851-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-192">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Message**","**CIM \_ алертиндикатион**.**Мессажеаргументс**")</span><span class="sxs-lookup"><span data-stu-id="48851-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-193">Уникальный идентификатор формата сообщений с областью организации, указанной в **овнинжентити**.</span><span class="sxs-lookup"><span data-stu-id="48851-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="48851-194">**осералертинжелементформат**</span><span class="sxs-lookup"><span data-stu-id="48851-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-197">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Алертинжелементформат**")</span><span class="sxs-lookup"><span data-stu-id="48851-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-198">Определяет формат свойства **алертингманажеделемент** , если свойство **алертинжелементформат** имеет значение "1" (другое); в противном случае это значение должно быть равно **null**.</span><span class="sxs-lookup"><span data-stu-id="48851-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="48851-199">**осералерттипе**</span><span class="sxs-lookup"><span data-stu-id="48851-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-200">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-202">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**AlertType**")</span><span class="sxs-lookup"><span data-stu-id="48851-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-203">Строка, описывающая значение **AlertType** , если свойство **AlertType** имеет значение 1 (другое изменение состояния).</span><span class="sxs-lookup"><span data-stu-id="48851-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="48851-204">**овнинжентити**</span><span class="sxs-lookup"><span data-stu-id="48851-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48851-207">Уникальный идентификатор организации, владеющей определением формата свойства **сообщения** .</span><span class="sxs-lookup"><span data-stu-id="48851-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="48851-208">**Овнинжентити** должен включать в себя авторские права, или уникальное имя, которое принадлежит бизнес-сущности или основному стандарту, заданному в формате сообщения.</span><span class="sxs-lookup"><span data-stu-id="48851-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="48851-209">**перцеиведсеверити**</span><span class="sxs-lookup"><span data-stu-id="48851-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-210">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48851-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48851-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-212">Квалификаторы: [**обязательный**](/windows/desktop/WmiSdk/standard-qualifiers), [**переопределенный**](/windows/desktop/WmiSdk/standard-qualifiers) ("Перцеиведсеверити"), [**МАППИНГСТРИНГС**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Наблюдаемая серьезность ")</span><span class="sxs-lookup"><span data-stu-id="48851-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="48851-213">Серьезность индикации предупреждения с точки зрения элемента, вызвавшего предупреждение.</span><span class="sxs-lookup"><span data-stu-id="48851-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48851-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="48851-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48851-215">Соответствует распространенному использованию.</span><span class="sxs-lookup"><span data-stu-id="48851-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48851-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="48851-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="48851-217">Указывает, что значение серьезности можно найти в свойстве Осерсеверити.</span><span class="sxs-lookup"><span data-stu-id="48851-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="48851-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Информация** (2)</span><span class="sxs-lookup"><span data-stu-id="48851-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="48851-219">Соответствует распространенному использованию.</span><span class="sxs-lookup"><span data-stu-id="48851-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="48851-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Снижение уровня работоспособности/предупреждение** (3)</span><span class="sxs-lookup"><span data-stu-id="48851-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="48851-221">Следует использовать, если нужно, чтобы пользователь мог решить, требуется ли действие.</span><span class="sxs-lookup"><span data-stu-id="48851-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="48851-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Дополнительный** (4)</span><span class="sxs-lookup"><span data-stu-id="48851-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="48851-223">Указывает, что требуется действие, но в настоящее время ситуация не является серьезной.</span><span class="sxs-lookup"><span data-stu-id="48851-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="48851-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Основной** (5)</span><span class="sxs-lookup"><span data-stu-id="48851-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="48851-225">Указывает, что требуется действие.</span><span class="sxs-lookup"><span data-stu-id="48851-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="48851-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (6)</span><span class="sxs-lookup"><span data-stu-id="48851-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="48851-227">Требуется действие, и область является широкой (возможно, это приведет к появлению случайного сбоя для критического ресурса).</span><span class="sxs-lookup"><span data-stu-id="48851-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="48851-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Неустранимый или невосстанавливаемый** (7)</span><span class="sxs-lookup"><span data-stu-id="48851-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="48851-229">Указывает, что произошла ошибка, но слишком поздно для выполнения действия по воспроизведению мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="48851-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="48851-230">**пробаблекаусе**</span><span class="sxs-lookup"><span data-stu-id="48851-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-231">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48851-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48851-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-233">Квалификаторы: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Вероятная причина: "," рекомендация. ITU \| M3100. пробаблекаусе "," ITU-IANA-Alarm-TC "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Пробаблекауседескриптион**","**CIM \_ алертиндикатион**.**EventID**","**CIM \_ алертиндикатион**.**EventTime**")</span><span class="sxs-lookup"><span data-stu-id="48851-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-234">Вероятная причина ситуации, которая привела к появлению предупреждения.</span><span class="sxs-lookup"><span data-stu-id="48851-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48851-235">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="48851-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="48851-236">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="48851-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="48851-237">**Ошибка адаптера или карты** (2)</span><span class="sxs-lookup"><span data-stu-id="48851-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="48851-238">**Сбой подсистемы приложения** (3)</span><span class="sxs-lookup"><span data-stu-id="48851-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="48851-239">**Полоса пропускания снижена** (4)</span><span class="sxs-lookup"><span data-stu-id="48851-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="48851-240">**Ошибка установки соединения** (5)</span><span class="sxs-lookup"><span data-stu-id="48851-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="48851-241">**Ошибка протокола связи** (6)</span><span class="sxs-lookup"><span data-stu-id="48851-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="48851-242">**Сбой подсистемы связи** (7)</span><span class="sxs-lookup"><span data-stu-id="48851-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="48851-243">**Ошибка настройки или настройки** (8)</span><span class="sxs-lookup"><span data-stu-id="48851-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="48851-244">**Перегрузка** (9)</span><span class="sxs-lookup"><span data-stu-id="48851-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="48851-245">**Поврежденные данные** (10)</span><span class="sxs-lookup"><span data-stu-id="48851-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="48851-246">**Превышен предел циклов ЦП** (11)</span><span class="sxs-lookup"><span data-stu-id="48851-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="48851-247">**Набор данных/ошибка модема** (12)</span><span class="sxs-lookup"><span data-stu-id="48851-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="48851-248">**Сигнал пониженной функциональности** (13)</span><span class="sxs-lookup"><span data-stu-id="48851-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="48851-249">**DTE-ошибка интерфейса DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="48851-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="48851-250">**Открыта дверца корпуса** (15)</span><span class="sxs-lookup"><span data-stu-id="48851-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="48851-251">**Неисправность оборудования** (16)</span><span class="sxs-lookup"><span data-stu-id="48851-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="48851-252">**Чрезмерная вибрация** (17)</span><span class="sxs-lookup"><span data-stu-id="48851-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="48851-253">**Ошибка формата файла** (18)</span><span class="sxs-lookup"><span data-stu-id="48851-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="48851-254">**Обнаружена Пожарная** программа (19)</span><span class="sxs-lookup"><span data-stu-id="48851-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="48851-255">**Обнаружен Flood** (20)</span><span class="sxs-lookup"><span data-stu-id="48851-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="48851-256">**Ошибка кадрирования** (21)</span><span class="sxs-lookup"><span data-stu-id="48851-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="48851-257">**Проблема с кондиционированием** (22)</span><span class="sxs-lookup"><span data-stu-id="48851-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="48851-258">**Недопустимая влажность** (23)</span><span class="sxs-lookup"><span data-stu-id="48851-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="48851-259">**Ошибка устройства ввода-вывода** (24)</span><span class="sxs-lookup"><span data-stu-id="48851-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="48851-260">**Ошибка устройства ввода** (25)</span><span class="sxs-lookup"><span data-stu-id="48851-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="48851-261">**Ошибка локальной сети** (26)</span><span class="sxs-lookup"><span data-stu-id="48851-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="48851-262">**Обнаружена Нетоксичнуюная утечка** (27)</span><span class="sxs-lookup"><span data-stu-id="48851-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="48851-263">**Ошибка передачи локального узла** (28)</span><span class="sxs-lookup"><span data-stu-id="48851-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="48851-264">**Потери кадра** (29)</span><span class="sxs-lookup"><span data-stu-id="48851-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="48851-265">**Потери сигнала** (30)</span><span class="sxs-lookup"><span data-stu-id="48851-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="48851-266">**Исчерпана заставка материалов** (31)</span><span class="sxs-lookup"><span data-stu-id="48851-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="48851-267">**Проблема мультиплексора** (32)</span><span class="sxs-lookup"><span data-stu-id="48851-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="48851-268">**Недостаточно памяти** (33)</span><span class="sxs-lookup"><span data-stu-id="48851-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="48851-269">**Ошибка устройства вывода** (34)</span><span class="sxs-lookup"><span data-stu-id="48851-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="48851-270">Снижение **производительности** (35)</span><span class="sxs-lookup"><span data-stu-id="48851-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="48851-271">**Проблема с питанием** (36)</span><span class="sxs-lookup"><span data-stu-id="48851-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="48851-272">**Неприемлемое давление** (37)</span><span class="sxs-lookup"><span data-stu-id="48851-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="48851-273">**Проблема с процессором (внутренняя ошибка компьютера)** (38)</span><span class="sxs-lookup"><span data-stu-id="48851-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="48851-274">**Сбой насоса** (39)</span><span class="sxs-lookup"><span data-stu-id="48851-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="48851-275">**Превышен размер очереди** (40)</span><span class="sxs-lookup"><span data-stu-id="48851-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="48851-276">**Сбой получения** (41)</span><span class="sxs-lookup"><span data-stu-id="48851-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="48851-277">**Сбой получателя** (42)</span><span class="sxs-lookup"><span data-stu-id="48851-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="48851-278">**Ошибка передачи удаленного узла** (43)</span><span class="sxs-lookup"><span data-stu-id="48851-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="48851-279">**Ресурсы с емкостью или с приближением** (44)</span><span class="sxs-lookup"><span data-stu-id="48851-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="48851-280">**Чрезмерное время ответа** (45)</span><span class="sxs-lookup"><span data-stu-id="48851-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="48851-281">**Чрезмерная частота** повторной передачи (46)</span><span class="sxs-lookup"><span data-stu-id="48851-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="48851-282">**Ошибка программного обеспечения** (47)</span><span class="sxs-lookup"><span data-stu-id="48851-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="48851-283">**Программное обеспечение аварийно завершено** (48)</span><span class="sxs-lookup"><span data-stu-id="48851-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="48851-284">**Ошибка программного обеспечения (неправильные результаты)** (49)</span><span class="sxs-lookup"><span data-stu-id="48851-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="48851-285">**Проблема с емкостью хранилища** (50)</span><span class="sxs-lookup"><span data-stu-id="48851-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="48851-286">**Недопустимая температура** (51)</span><span class="sxs-lookup"><span data-stu-id="48851-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="48851-287">**Пересечение пороговых значений** (52)</span><span class="sxs-lookup"><span data-stu-id="48851-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="48851-288">**Проблема синхронизации** (53)</span><span class="sxs-lookup"><span data-stu-id="48851-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="48851-289">**Обнаружена утечка токсичную** (54)</span><span class="sxs-lookup"><span data-stu-id="48851-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="48851-290">**Сбой передачи** (55)</span><span class="sxs-lookup"><span data-stu-id="48851-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="48851-291">**Сбой передатчика** (56)</span><span class="sxs-lookup"><span data-stu-id="48851-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="48851-292">**Базовый ресурс недоступен** (57)</span><span class="sxs-lookup"><span data-stu-id="48851-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="48851-293">**Несоответствие версий** (58)</span><span class="sxs-lookup"><span data-stu-id="48851-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="48851-294">**Предыдущее оповещение сброшено** (59)</span><span class="sxs-lookup"><span data-stu-id="48851-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="48851-295">**Неудачные попытки входа** (60)</span><span class="sxs-lookup"><span data-stu-id="48851-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="48851-296">**Обнаружен вирус по** (61)</span><span class="sxs-lookup"><span data-stu-id="48851-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="48851-297">**Нарушение безопасности оборудования** (62)</span><span class="sxs-lookup"><span data-stu-id="48851-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="48851-298">**Обнаружен отказ в обслуживании** (63)</span><span class="sxs-lookup"><span data-stu-id="48851-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="48851-299">**Несоответствие учетных данных безопасности** (64)</span><span class="sxs-lookup"><span data-stu-id="48851-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="48851-300">**Несанкционированный доступ** (65)</span><span class="sxs-lookup"><span data-stu-id="48851-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="48851-301">**Получен сигнал** (66)</span><span class="sxs-lookup"><span data-stu-id="48851-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="48851-302">**Потери указателя** (67)</span><span class="sxs-lookup"><span data-stu-id="48851-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="48851-303">**Несовпадение полезных данных** (68)</span><span class="sxs-lookup"><span data-stu-id="48851-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="48851-304">**Ошибка передачи** (69)</span><span class="sxs-lookup"><span data-stu-id="48851-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="48851-305">**Чрезмерная частота ошибок** (70)</span><span class="sxs-lookup"><span data-stu-id="48851-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="48851-306">**Проблема трассировки** (71)</span><span class="sxs-lookup"><span data-stu-id="48851-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="48851-307">**Элемент недоступен** (72)</span><span class="sxs-lookup"><span data-stu-id="48851-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="48851-308">**Отсутствует элемент** (73)</span><span class="sxs-lookup"><span data-stu-id="48851-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="48851-309">**Потери нескольких кадров** (74)</span><span class="sxs-lookup"><span data-stu-id="48851-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="48851-310">**Сбой широковещательного канала** (75)</span><span class="sxs-lookup"><span data-stu-id="48851-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="48851-311">**Получено недопустимое сообщение** (76)</span><span class="sxs-lookup"><span data-stu-id="48851-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="48851-312">**Сбой маршрутизации** (77)</span><span class="sxs-lookup"><span data-stu-id="48851-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="48851-313">**Сбой объединительной платы** (78)</span><span class="sxs-lookup"><span data-stu-id="48851-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="48851-314">**Дублирование идентификаторов** (79)</span><span class="sxs-lookup"><span data-stu-id="48851-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="48851-315">**Сбой пути защиты** (80)</span><span class="sxs-lookup"><span data-stu-id="48851-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="48851-316">**Потери или несоответствие синхронизации** (81)</span><span class="sxs-lookup"><span data-stu-id="48851-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="48851-317">**Проблема с терминалом** (82)</span><span class="sxs-lookup"><span data-stu-id="48851-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="48851-318">**Сбой часов реального времени** (83)</span><span class="sxs-lookup"><span data-stu-id="48851-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="48851-319">**Сбой антенны** (84)</span><span class="sxs-lookup"><span data-stu-id="48851-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="48851-320">**Сбой зарядки аккумулятора** (85)</span><span class="sxs-lookup"><span data-stu-id="48851-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="48851-321">**Сбой диска** (86)</span><span class="sxs-lookup"><span data-stu-id="48851-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="48851-322">**Частота сбоев прыгающее»** (87)</span><span class="sxs-lookup"><span data-stu-id="48851-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="48851-323">**Потери избыточности** (88)</span><span class="sxs-lookup"><span data-stu-id="48851-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="48851-324">**Сбой источника питания** (89)</span><span class="sxs-lookup"><span data-stu-id="48851-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="48851-325">**Проблема качества сигнала** (90)</span><span class="sxs-lookup"><span data-stu-id="48851-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="48851-326">**Заряд аккумулятора** (91)</span><span class="sxs-lookup"><span data-stu-id="48851-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="48851-327">**Сбой аккумулятора** (92)</span><span class="sxs-lookup"><span data-stu-id="48851-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="48851-328">**Коммерческая проблема электропитания** (93)</span><span class="sxs-lookup"><span data-stu-id="48851-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="48851-329">**Сбой вентилятора** (94)</span><span class="sxs-lookup"><span data-stu-id="48851-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="48851-330">**Сбой подсистемы** (95)</span><span class="sxs-lookup"><span data-stu-id="48851-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="48851-331">**Сбой датчика** (96)</span><span class="sxs-lookup"><span data-stu-id="48851-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="48851-332">**Сбой предохранителя** (97)</span><span class="sxs-lookup"><span data-stu-id="48851-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="48851-333">**Сбой генератора** (98)</span><span class="sxs-lookup"><span data-stu-id="48851-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="48851-334">**Низкий аккумулятор** (99)</span><span class="sxs-lookup"><span data-stu-id="48851-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="48851-335">**Низкое топливо** (100)</span><span class="sxs-lookup"><span data-stu-id="48851-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="48851-336">**Нижняя вода** (101)</span><span class="sxs-lookup"><span data-stu-id="48851-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="48851-337">**Взрывной газ** (102)</span><span class="sxs-lookup"><span data-stu-id="48851-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="48851-338">**High подойдет к концу** (103)</span><span class="sxs-lookup"><span data-stu-id="48851-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="48851-339">**ICE накрутки** (104)</span><span class="sxs-lookup"><span data-stu-id="48851-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="48851-340">**Тест состояния** (105)</span><span class="sxs-lookup"><span data-stu-id="48851-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="48851-341">**Несоответствие памяти** (106)</span><span class="sxs-lookup"><span data-stu-id="48851-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="48851-342">**Недостаточно циклов ЦП** (107)</span><span class="sxs-lookup"><span data-stu-id="48851-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="48851-343">**Проблема программной среды** (108)</span><span class="sxs-lookup"><span data-stu-id="48851-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="48851-344">**Сбой загрузки программного обеспечения** (109)</span><span class="sxs-lookup"><span data-stu-id="48851-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="48851-345">**Элемент повторно инициализирован** (110)</span><span class="sxs-lookup"><span data-stu-id="48851-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="48851-346">**Время ожидания** (111)</span><span class="sxs-lookup"><span data-stu-id="48851-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="48851-347">**Регистрация проблем** (112)</span><span class="sxs-lookup"><span data-stu-id="48851-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="48851-348">**Обнаружена утечка** (113)</span><span class="sxs-lookup"><span data-stu-id="48851-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="48851-349">**Сбой механизма защиты** (114)</span><span class="sxs-lookup"><span data-stu-id="48851-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="48851-350">**Сбой защиты ресурса** (115)</span><span class="sxs-lookup"><span data-stu-id="48851-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="48851-351">**Несогласованность базы данных** (116)</span><span class="sxs-lookup"><span data-stu-id="48851-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="48851-352">**Сбой проверки подлинности** (117)</span><span class="sxs-lookup"><span data-stu-id="48851-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="48851-353">**Нарушение конфиденциальности** (118)</span><span class="sxs-lookup"><span data-stu-id="48851-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="48851-354">**Несанкционированный кабель** (119)</span><span class="sxs-lookup"><span data-stu-id="48851-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="48851-355">**Отложенная информация** (120)</span><span class="sxs-lookup"><span data-stu-id="48851-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="48851-356">**Дублирование данных** (121)</span><span class="sxs-lookup"><span data-stu-id="48851-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="48851-357">**Отсутствует информация** (122)</span><span class="sxs-lookup"><span data-stu-id="48851-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="48851-358">**Изменение сведений** (123)</span><span class="sxs-lookup"><span data-stu-id="48851-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="48851-359">**Непоследовательная информация** (124)</span><span class="sxs-lookup"><span data-stu-id="48851-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="48851-360">**Истек срок действия ключа** (125)</span><span class="sxs-lookup"><span data-stu-id="48851-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="48851-361">**Сбой отказа от отрицания** (126)</span><span class="sxs-lookup"><span data-stu-id="48851-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="48851-362">**Активность за нерабочее время** (127)</span><span class="sxs-lookup"><span data-stu-id="48851-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="48851-363">Не **обслуживается** (128)</span><span class="sxs-lookup"><span data-stu-id="48851-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="48851-364">**Процедурная ошибка** (129)</span><span class="sxs-lookup"><span data-stu-id="48851-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="48851-365">**Непредвиденные сведения** (130)</span><span class="sxs-lookup"><span data-stu-id="48851-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48851-366">**пробаблекауседескриптион**</span><span class="sxs-lookup"><span data-stu-id="48851-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-369">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ алертиндикатион**.**Пробаблекаусе**")</span><span class="sxs-lookup"><span data-stu-id="48851-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="48851-370">Дополнительные сведения, относящиеся к свойству **пробаблекаусе** .</span><span class="sxs-lookup"><span data-stu-id="48851-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="48851-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="48851-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-372">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-374">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="48851-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48851-375">Имя поставщика, который создал указание.</span><span class="sxs-lookup"><span data-stu-id="48851-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="48851-376">**рекоммендедактионс**</span><span class="sxs-lookup"><span data-stu-id="48851-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-377">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="48851-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="48851-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-379">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Предложенные действия по восстановлению ")</span><span class="sxs-lookup"><span data-stu-id="48851-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="48851-380">Бесплатные описания рекомендуемых действий, которые необходимо выполнить для устранения причины уведомления.</span><span class="sxs-lookup"><span data-stu-id="48851-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="48851-381">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="48851-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-384">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="48851-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48851-385">Значение **CreationClassName** системы для поставщика, который создал указание.</span><span class="sxs-lookup"><span data-stu-id="48851-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="48851-386">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="48851-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="48851-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48851-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-389">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="48851-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="48851-390">Системное имя поставщика, создавшего указание.</span><span class="sxs-lookup"><span data-stu-id="48851-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="48851-391">**Тренды**</span><span class="sxs-lookup"><span data-stu-id="48851-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48851-392">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="48851-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="48851-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="48851-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48851-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Трендиндикатион ")</span><span class="sxs-lookup"><span data-stu-id="48851-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="48851-395">Содержит сведения о тенденциях — тенденция вверх, вниз или без изменений.</span><span class="sxs-lookup"><span data-stu-id="48851-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="48851-396">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="48851-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="48851-397">**Неприменимо** (1)</span><span class="sxs-lookup"><span data-stu-id="48851-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="48851-398">**Тенденция вверх** (2)</span><span class="sxs-lookup"><span data-stu-id="48851-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="48851-399">**Тенденция вниз** (3)</span><span class="sxs-lookup"><span data-stu-id="48851-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="48851-400">**Без изменений** (4)</span><span class="sxs-lookup"><span data-stu-id="48851-400">**No Change** (4)</span></span>


<span data-ttu-id="48851-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="48851-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="48851-402">Требования</span><span class="sxs-lookup"><span data-stu-id="48851-402">Requirements</span></span>



| <span data-ttu-id="48851-403">Требование</span><span class="sxs-lookup"><span data-stu-id="48851-403">Requirement</span></span> | <span data-ttu-id="48851-404">Значение</span><span class="sxs-lookup"><span data-stu-id="48851-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48851-405">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48851-405">Minimum supported client</span></span><br/> | <span data-ttu-id="48851-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="48851-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="48851-407">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48851-407">Minimum supported server</span></span><br/> | <span data-ttu-id="48851-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="48851-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="48851-409">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="48851-409">Namespace</span></span><br/>                | <span data-ttu-id="48851-410">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="48851-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48851-411">MOF</span><span class="sxs-lookup"><span data-stu-id="48851-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48851-412"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48851-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48851-413">DLL</span><span class="sxs-lookup"><span data-stu-id="48851-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48851-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48851-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48851-415">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48851-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48851-416">**\_ПРОЦЕССИНДИКАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="48851-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

