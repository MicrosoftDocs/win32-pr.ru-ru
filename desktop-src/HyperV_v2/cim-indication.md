---
description: '\_Указание CIM является абстрактным базовым классом для всех уведомлений об изменениях в объектах схемы и данных объектов схемы, событиях, обнаруженных поставщиками и инструментированием. Подклассы индикации CIM \_ представляют конкретные типы уведомлений.'
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: Класс CIM_Indication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683308"
---
# <a name="cim_indication-class"></a><span data-ttu-id="16c26-104">\_Класс индикации CIM</span><span class="sxs-lookup"><span data-stu-id="16c26-104">CIM\_Indication class</span></span>

<span data-ttu-id="16c26-105">**Модель CIM \_ Указание** является абстрактным базовым классом для всех уведомлений об изменениях в объектах схемы и данных объектов схемы, событиях, обнаруженных поставщиками и инструментированием.</span><span class="sxs-lookup"><span data-stu-id="16c26-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="16c26-106">Подклассы **\_ индикации CIM** представляют конкретные типы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="16c26-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="16c26-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16c26-107">Syntax</span></span>

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a><span data-ttu-id="16c26-108">Члены</span><span class="sxs-lookup"><span data-stu-id="16c26-108">Members</span></span>

<span data-ttu-id="16c26-109">Класс **\_ индикации CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="16c26-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="16c26-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="16c26-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16c26-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="16c26-111">Properties</span></span>

<span data-ttu-id="16c26-112">Класс **\_ индикации CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="16c26-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16c26-113">**коррелатединдикатионс**</span><span class="sxs-lookup"><span data-stu-id="16c26-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-114">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="16c26-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="16c26-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-116">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Коррелированные уведомления "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ индикатор CIM**.**Индикатионидентифиер**")</span><span class="sxs-lookup"><span data-stu-id="16c26-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-117">Массив, содержащий **индикатионидентифиер** значения уведомлений, связанных с данным.</span><span class="sxs-lookup"><span data-stu-id="16c26-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="16c26-118">**индикатионфилтернаме**</span><span class="sxs-lookup"><span data-stu-id="16c26-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="16c26-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-121">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")</span><span class="sxs-lookup"><span data-stu-id="16c26-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-122">Идентификатор фильтра индикации, который обрабатывает индикацию.</span><span class="sxs-lookup"><span data-stu-id="16c26-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="16c26-123">Служба отправки задает это свойство.</span><span class="sxs-lookup"><span data-stu-id="16c26-123">The sending service sets this property.</span></span> <span data-ttu-id="16c26-124">Это свойство соотносится со свойством **Name** объекта **CIM \_ индикатионфилтер** .</span><span class="sxs-lookup"><span data-stu-id="16c26-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="16c26-125">Значение **индикатионфилтернаме** должно иметь следующий формат:</span><span class="sxs-lookup"><span data-stu-id="16c26-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="16c26-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="16c26-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="16c26-127">*<OrgID>* должен содержать имя, которое принадлежит бизнес-сущности, владеющей объектом.</span><span class="sxs-lookup"><span data-stu-id="16c26-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="16c26-128">*<OrgID>* не должно содержать двоеточие (:)</span><span class="sxs-lookup"><span data-stu-id="16c26-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="16c26-129">*<LocalID>* уникальный идентификатор, выбранный бизнес-сущностью, которой принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="16c26-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="16c26-130">**индикатионидентифиер**</span><span class="sxs-lookup"><span data-stu-id="16c26-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="16c26-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Идентификатор уведомления ")</span><span class="sxs-lookup"><span data-stu-id="16c26-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-134">Идентификатор индикации.</span><span class="sxs-lookup"><span data-stu-id="16c26-134">An identifier of the indication.</span></span> <span data-ttu-id="16c26-135">Это свойство можно использовать в качестве значения ключа в массиве свойств **коррелатединдикатионс** .</span><span class="sxs-lookup"><span data-stu-id="16c26-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="16c26-136">Таким образом, **индикатионидентифиер** должно быть уникальным значением в пространстве имен этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="16c26-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="16c26-137">Чтобы убедиться, что **индикатионидентифиер** является уникальным, он должен использовать следующий формат:</span><span class="sxs-lookup"><span data-stu-id="16c26-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="16c26-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="16c26-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="16c26-139">*<OrgID>* должен содержать имя, которое принадлежит бизнес-сущности, владеющей объектом.</span><span class="sxs-lookup"><span data-stu-id="16c26-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="16c26-140">*<OrgID>* не должно содержать двоеточие (:)</span><span class="sxs-lookup"><span data-stu-id="16c26-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="16c26-141">*<LocalID>* уникальный идентификатор, выбранный бизнес-сущностью, которой принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="16c26-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="16c26-142">Для экземпляров, определенных DMTF, *<OrgID>* следует задать значение "CIM".</span><span class="sxs-lookup"><span data-stu-id="16c26-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="16c26-143">**индикатионтиме**</span><span class="sxs-lookup"><span data-stu-id="16c26-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-144">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="16c26-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16c26-146">Дата и время создания указания.</span><span class="sxs-lookup"><span data-stu-id="16c26-146">The time and date when the indication was created.</span></span> <span data-ttu-id="16c26-147">Свойство может иметь значение **null** , если сущность, создавшая указание, не может определить эту информацию.</span><span class="sxs-lookup"><span data-stu-id="16c26-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="16c26-148">Значение **индикатионтиме** может быть одинаковым для обозначений, которые создаются в ходе быстрой успешной операции.</span><span class="sxs-lookup"><span data-stu-id="16c26-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="16c26-149">**осерсеверити**</span><span class="sxs-lookup"><span data-stu-id="16c26-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="16c26-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-152">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ алертиндикатион**](cim-alertindication.md).**Перцеиведсеверити**")</span><span class="sxs-lookup"><span data-stu-id="16c26-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-153">Степень серьезности обозначения от точки зрения уведомления, когда **перцеиведсеверити** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="16c26-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="16c26-154">**перцеиведсеверити**</span><span class="sxs-lookup"><span data-stu-id="16c26-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-155">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16c26-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-157">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("рекомендация. ITU \| X733. Наблюдаемая серьезность ")</span><span class="sxs-lookup"><span data-stu-id="16c26-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-158">Серьезность индикации от точки зрения уведомления.</span><span class="sxs-lookup"><span data-stu-id="16c26-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="16c26-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="16c26-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-160">Наблюдаемая степень серьезности индикации неизвестна или неопределена.</span><span class="sxs-lookup"><span data-stu-id="16c26-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="16c26-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="16c26-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-162">Указывает, что значение серьезности можно найти в свойстве **осерсеверити** .</span><span class="sxs-lookup"><span data-stu-id="16c26-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="16c26-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Информация** (2)</span><span class="sxs-lookup"><span data-stu-id="16c26-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-164">При предоставлении информативного ответа следует использовать сведения.</span><span class="sxs-lookup"><span data-stu-id="16c26-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="16c26-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Снижение уровня работоспособности/предупреждение** (3)</span><span class="sxs-lookup"><span data-stu-id="16c26-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-166">Следует использовать, если нужно, чтобы пользователь мог решить, требуется ли действие.</span><span class="sxs-lookup"><span data-stu-id="16c26-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="16c26-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Дополнительный** (4)</span><span class="sxs-lookup"><span data-stu-id="16c26-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-168">Требуется действие, но в настоящее время ситуация не является серьезной.</span><span class="sxs-lookup"><span data-stu-id="16c26-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="16c26-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Основной** (5)</span><span class="sxs-lookup"><span data-stu-id="16c26-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-170">Теперь требуется действие.</span><span class="sxs-lookup"><span data-stu-id="16c26-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="16c26-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (6)</span><span class="sxs-lookup"><span data-stu-id="16c26-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-172">Требуется действие, и область является широкой (возможно, это приведет к появлению случайного сбоя для критического ресурса).</span><span class="sxs-lookup"><span data-stu-id="16c26-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="16c26-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Неустранимый или невосстанавливаемый** (7)</span><span class="sxs-lookup"><span data-stu-id="16c26-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="16c26-174">произошла ошибка, но слишком поздно для выполнения действия по воспроизведению мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="16c26-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="16c26-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="16c26-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="16c26-176">**секуенцеконтекст**</span><span class="sxs-lookup"><span data-stu-id="16c26-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="16c26-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-179">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ признак CIM**".**SequenceNumber**")</span><span class="sxs-lookup"><span data-stu-id="16c26-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-180">Контекст последовательности идентификаторов последовательности для индикации.</span><span class="sxs-lookup"><span data-stu-id="16c26-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="16c26-181">Если служба не поддерживает идентификаторы последовательности для указаний, это свойство должно иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="16c26-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="16c26-182">Если передается перепоставка, это свойство остается прежним.</span><span class="sxs-lookup"><span data-stu-id="16c26-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="16c26-183">Идентификатор последовательности для указания позволяет прослушивателю определять дублированные указания, когда служба пытается повторно доставить события, изменить порядок следования и обнаружить потерянные события.</span><span class="sxs-lookup"><span data-stu-id="16c26-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="16c26-184">Чтобы убедиться, что **секуенцеконтекст** является уникальным, он должен использовать следующий формат:</span><span class="sxs-lookup"><span data-stu-id="16c26-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="16c26-185">*обозначение-Service-Name* \# *CIM-Service-Start-ID* \# *прослушиватель — время создания*</span><span class="sxs-lookup"><span data-stu-id="16c26-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="16c26-186">*обозначение-Service-Name* — это значение свойства **Name** экземпляра **CIM \_ индикатионсервице** , который доставляет указание.</span><span class="sxs-lookup"><span data-stu-id="16c26-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="16c26-187">*CIM-Service-Start-ID* — это идентификатор, который однозначно определяет начальную операцию службы.</span><span class="sxs-lookup"><span data-stu-id="16c26-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="16c26-188">Например, это может быть метка времени начала или счетчик, увеличивающийся для каждого запуска или перезапуска службы.</span><span class="sxs-lookup"><span data-stu-id="16c26-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="16c26-189">*время создания прослушивателя-места назначения* — это метка времени создания экземпляра **\_ листенердестинатион CIM** , представляющего назначение прослушивателя. нсинце этот формат является только рекомендацией, клиенты CIM считают это значение непрозрачным идентификатором для контекста последовательности и не должны полагаться на этот формат.</span><span class="sxs-lookup"><span data-stu-id="16c26-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="16c26-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="16c26-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16c26-191">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="16c26-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="16c26-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="16c26-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16c26-193">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ признак CIM**".**Секуенцеконтекст**")</span><span class="sxs-lookup"><span data-stu-id="16c26-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="16c26-194">Порядковый номер идентификатора последовательности для указания.</span><span class="sxs-lookup"><span data-stu-id="16c26-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="16c26-195">Идентификатор последовательности для указания позволяет прослушивателю определять дублированные указания, когда служба пытается повторно доставить события, изменить порядок следования и обнаружить потерянные события.</span><span class="sxs-lookup"><span data-stu-id="16c26-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="16c26-196">Порядковый номер имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="16c26-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="16c26-197">Порядковый номер сбрасывается в "0" при каждом изменении значения **секуенцеконтекст** .</span><span class="sxs-lookup"><span data-stu-id="16c26-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="16c26-198">Каждый раз, когда назначение прослушивателя получает новую индикацию, порядковый номер увеличивается на 1.</span><span class="sxs-lookup"><span data-stu-id="16c26-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="16c26-199">Порядковый номер переносится в "0" при превышении диапазона значений.</span><span class="sxs-lookup"><span data-stu-id="16c26-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="16c26-200">Если индикатор доставляется снова, **SequenceNumber** остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="16c26-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16c26-201">Требования</span><span class="sxs-lookup"><span data-stu-id="16c26-201">Requirements</span></span>



| <span data-ttu-id="16c26-202">Требование</span><span class="sxs-lookup"><span data-stu-id="16c26-202">Requirement</span></span> | <span data-ttu-id="16c26-203">Значение</span><span class="sxs-lookup"><span data-stu-id="16c26-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16c26-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16c26-204">Minimum supported client</span></span><br/> | <span data-ttu-id="16c26-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16c26-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="16c26-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16c26-206">Minimum supported server</span></span><br/> | <span data-ttu-id="16c26-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="16c26-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="16c26-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="16c26-208">Namespace</span></span><br/>                | <span data-ttu-id="16c26-209">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="16c26-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="16c26-210">MOF</span><span class="sxs-lookup"><span data-stu-id="16c26-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16c26-211"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16c26-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16c26-212">DLL</span><span class="sxs-lookup"><span data-stu-id="16c26-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c26-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16c26-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16c26-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16c26-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c26-215">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="16c26-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

