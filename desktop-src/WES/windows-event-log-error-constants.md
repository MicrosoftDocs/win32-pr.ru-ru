---
title: Константы ошибки журнала событий Windows (WinError. h)
description: Ниже приведены коды ошибок, которые определяет журнал событий Windows.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5443d98c53d6abedbe3a0027e8e2e524ae9df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691930"
---
# <a name="windows-event-log-error-constants"></a><span data-ttu-id="e4b2b-103">Константы ошибки журнала событий Windows</span><span class="sxs-lookup"><span data-stu-id="e4b2b-103">Windows Event Log Error Constants</span></span>

<span data-ttu-id="e4b2b-104">Ниже приведены коды ошибок, которые определяет журнал событий Windows.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-104">The following are the error codes that Windows Event Log defines.</span></span>

<dl> <dt>

<span data-ttu-id="e4b2b-105"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**Ошибка \_ evt \_ недопустимого \_ \_ пути канала**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-105"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-106">15 000</span><span class="sxs-lookup"><span data-stu-id="e4b2b-106">15000</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-107">Указан недопустимый путь к каналу.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-107">The specified channel path is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-108"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**Ошибка \_ \_ недопустимого \_ запроса evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-108"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-109">15001</span><span class="sxs-lookup"><span data-stu-id="e4b2b-109">15001</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-110">Указан недопустимый запрос.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-110">The specified query is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-111"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**Ошибка \_ \_ \_ \_ не найдены метаданные издателя \_ evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-111"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-112">15002</span><span class="sxs-lookup"><span data-stu-id="e4b2b-112">15002</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-113">Не удается найти метаданные поставщика в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-113">The provider metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-114"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ шаблон событий Error \_ evt \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-114"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-115">15003</span><span class="sxs-lookup"><span data-stu-id="e4b2b-115">15003</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-116">Не удается найти шаблон для определения события в ресурсе.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-116">The template for an event definition cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-117"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**Ошибка \_ evt \_ недопустимое \_ \_ имя издателя**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-117"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-118">15004</span><span class="sxs-lookup"><span data-stu-id="e4b2b-118">15004</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-119">Указано недопустимое имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-119">The specified provider name is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-120"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**Ошибка \_ evt " \_ недопустимые \_ \_ данные события"**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-120"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-121">15005</span><span class="sxs-lookup"><span data-stu-id="e4b2b-121">15005</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-122">Данные события, вызванные поставщиком, несовместимы с определением шаблона события в манифесте поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-122">The event data raised by the provider is not compatible with the event template definition in the provider's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-123"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_канал ошибки \_ evt \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-123"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-124">15007</span><span class="sxs-lookup"><span data-stu-id="e4b2b-124">15007</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-125">Не удается найти указанный канал.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-125">The specified channel cannot be found.</span></span> <span data-ttu-id="e4b2b-126">Проверьте конфигурацию канала.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-126">Check the channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-127"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**Ошибка \_ evt \_ неправильно сформированный \_ XML- \_ текст**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-127"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-128">15008</span><span class="sxs-lookup"><span data-stu-id="e4b2b-128">15008</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-129">Указанный XML-текст имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-129">The specified XML text was not well-formed.</span></span> <span data-ttu-id="e4b2b-130">Для получения дополнительных сведений вызовите функцию [**евтжетекстендедстатус**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .</span><span class="sxs-lookup"><span data-stu-id="e4b2b-130">For more information, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-131"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**Ошибка \_ при \_ подписке evt \_ на \_ прямой \_ канал**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-131"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-132">15009</span><span class="sxs-lookup"><span data-stu-id="e4b2b-132">15009</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-133">Нельзя подписываться на аналитический или отладочный канал; события для аналитического или отладочного канала попадают непосредственно в файл журнала и не могут быть подписаны на.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-133">You cannot subscribe to an Analytic or Debug channel; the events for an Analytic or Debug channel go directly to a log file and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-134"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**Ошибка \_ \_ конфигурации evt \_**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-134"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-135">15010</span><span class="sxs-lookup"><span data-stu-id="e4b2b-135">15010</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-136">Произошла ошибка конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-136">A configuration error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-137"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**\_ \_ \_ неактуальный результат \_ запроса "ошибка evt"**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-137"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-138">15011</span><span class="sxs-lookup"><span data-stu-id="e4b2b-138">15011</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-139">Недопустимый результат запроса.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-139">The query result is not valid.</span></span> <span data-ttu-id="e4b2b-140">Это может быть вызвано очисткой или перебором журнала после создания результата запроса.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-140">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="e4b2b-141">Освободите объект результата запроса и повторите запрос.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-141">Release the query result object and reissue the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-142"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ошибочное \_ \_ \_ значение результата \_ запроса \_ "ошибка evt"**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-142"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-143">15012</span><span class="sxs-lookup"><span data-stu-id="e4b2b-143">15012</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-144">Курсор для результата запроса не указывает на допустимую позицию.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-144">The cursor for the query result is not pointing to a valid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-145"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**Ошибка \_ EVT, \_ не \_ проверяющая \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-145"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-146">15013</span><span class="sxs-lookup"><span data-stu-id="e4b2b-146">15013</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-147">Зарегистрированный синтаксический анализатор MSXML не поддерживает проверку.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-147">The registered MSXML parser does not support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-148"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**Ошибка \_ evt \_ Filter \_ алреадископед**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-148"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-149">15014</span><span class="sxs-lookup"><span data-stu-id="e4b2b-149">15014</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-150">За выражением может следовать изменение операции Scope только в том случае, если результатом вычисления выражения является набор узлов и он еще не является частью какого-либо другого изменения операции с областью действия.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-150">An expression can be followed by a change of scope operation only if the expression evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-151"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**Ошибка \_ evt \_ Filter \_ нотелтсет**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-151"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-152">15015</span><span class="sxs-lookup"><span data-stu-id="e4b2b-152">15015</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-153">Невозможно выполнить шаг с термином, который не представляет набор элементов.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-153">Cannot perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-154"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**Ошибка \_ evt \_ Filter \_ инварг**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-154"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-155">15016</span><span class="sxs-lookup"><span data-stu-id="e4b2b-155">15016</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-156">Аргументы в левой части бинарного оператора должны быть либо атрибутами, либо узлами, либо переменными, а аргументы в правой части должны быть константами.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-156">The arguments on the left side of a binary operator must be either attributes, nodes, or variables, and the arguments on the right side must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-157"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**Ошибка \_ evt \_ Filter \_ инвтест**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-157"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-158">15017</span><span class="sxs-lookup"><span data-stu-id="e4b2b-158">15017</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-159">Операция шага должна затрагивать либо проверку узла, либо, в случае предиката, выражение алгебраические, для которого необходимо проверить каждый узел в наборе узлов, определяемый предыдущим набором узлов.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-159">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-160"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**Ошибка \_ evt \_ Filter \_ инвтипе**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-160"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-161">15018</span><span class="sxs-lookup"><span data-stu-id="e4b2b-161">15018</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-162">Этот тип данных не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-162">This data type not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-163"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**Ошибка \_ evt \_ Filter \_ парсирр**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-163"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-164">15019</span><span class="sxs-lookup"><span data-stu-id="e4b2b-164">15019</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-165">В указанной позиции произошла синтаксическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-165">A syntax error occurred at the specified position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-166"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**Ошибка \_ evt \_ Filter \_ унсуппортедоп**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-166"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-167">15020</span><span class="sxs-lookup"><span data-stu-id="e4b2b-167">15020</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-168">Этот оператор не поддерживается этой реализацией фильтра.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-168">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-169"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**Ошибка \_ evt \_ Filter \_ унекспектедтокен**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-169"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-170">15021</span><span class="sxs-lookup"><span data-stu-id="e4b2b-170">15021</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-171">Обнаружена непредвиденная лексема.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-171">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-172"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**Ошибка \_ evt \_ недопустимой \_ операции \_ через \_ включенный \_ прямой \_ канал**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-172"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-173">15022</span><span class="sxs-lookup"><span data-stu-id="e4b2b-173">15022</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-174">Запрошенную операцию нельзя выполнить через включенный аналитический или отладочный канал.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-174">The requested operation cannot be performed over an enabled Analytic or Debug channel.</span></span> <span data-ttu-id="e4b2b-175">Перед выполнением запрошенной операции необходимо отключить канал.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-175">You must disable the channel before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-176"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства канала \_**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-176"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-177">15023</span><span class="sxs-lookup"><span data-stu-id="e4b2b-177">15023</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-178">Свойство канала содержит недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-178">The channel property contains a value that is not valid.</span></span> <span data-ttu-id="e4b2b-179">Тип значения может быть недопустимым, значение может находиться вне допустимого диапазона, либо значение не может быть обновлено или не поддерживается для этого типа канала.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-179">The value's type may not be valid, the value may be out of range, or the value cannot be updated or is not supported for this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-180"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**Ошибка \_ evt \_ недопустимое \_ \_ значение свойства издателя \_**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-180"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-181">15024</span><span class="sxs-lookup"><span data-stu-id="e4b2b-181">15024</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-182">Свойство Provider содержит недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-182">The provider property contains a value that is not valid.</span></span> <span data-ttu-id="e4b2b-183">Тип значения может быть недопустимым, значение может находиться вне допустимого диапазона, либо значение не может быть обновлено или не поддерживается для данного типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-183">The value's type may not be valid, the value may be out of range, or the value cannot be updated or is not supported for this type of provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-184"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**Ошибка \_ при \_ \_ активации канала \_ evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-184"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-185">15025</span><span class="sxs-lookup"><span data-stu-id="e4b2b-185">15025</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-186">Не удалось активировать канал.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-186">The channel failed to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-187"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**\_ \_ \_ слишком \_ сложный фильтр evt ошибки**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-187"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-188">15026</span><span class="sxs-lookup"><span data-stu-id="e4b2b-188">15026</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-189">Выражение XPath превысило поддерживаемую сложность.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-189">The XPath expression exceeded supported complexity.</span></span> <span data-ttu-id="e4b2b-190">Упростите выражение или разделите его на два или более простых выражения.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-190">Simplify the expression or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-191"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**сообщение с ошибкой \_ evt \_ \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-191"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-192">15027</span><span class="sxs-lookup"><span data-stu-id="e4b2b-192">15027</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-193">Ресурс сообщения существует, но сообщение не найдено в строке или таблице сообщений.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-193">The message resource is present, but the message is not found in the string or message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-194"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ идентификатор сообщения ошибки \_ evt \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-194"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-195">15028</span><span class="sxs-lookup"><span data-stu-id="e4b2b-195">15028</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-196">Не удается найти идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-196">The message identifier cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-197"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**Ошибка \_ EVT, \_ неразрешенное \_ значение \_ INSERT**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-197"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-198">15029</span><span class="sxs-lookup"><span data-stu-id="e4b2b-198">15029</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-199">Не удается найти строку подстановки для индекса вставки.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-199">The substitution string for the insert index cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-200"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**Ошибка \_ EVT, \_ неразрешенная \_ \_ Вставка параметра**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-200"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-201">15030</span><span class="sxs-lookup"><span data-stu-id="e4b2b-201">15030</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-202">Не удается найти строку описания для ссылки на параметр (%1).</span><span class="sxs-lookup"><span data-stu-id="e4b2b-202">The description string for parameter reference (%1) cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-203"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**\_ \_ \_ достигнуто максимальное число вставок \_ ошибок evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-203"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-204">15031</span><span class="sxs-lookup"><span data-stu-id="e4b2b-204">15031</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-205">Достигнуто максимальное число замен.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-205">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-206"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_Определение события "ошибка evt" \_ \_ \_ не \_ Найдено**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-206"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-207">15032</span><span class="sxs-lookup"><span data-stu-id="e4b2b-207">15032</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-208">Не удается найти определение события для идентификатора события.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-208">The event definition cannot be found for the event identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-209"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ не удалось найти языковой стандарт сообщений \_ с ошибкой evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-209"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-210">15033</span><span class="sxs-lookup"><span data-stu-id="e4b2b-210">15033</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-211">Ресурс, зависящий от локали, для требуемого сообщения отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-211">The locale-specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-212"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**\_ \_ \_ слишком \_ старая версия evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-212"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-213">15034</span><span class="sxs-lookup"><span data-stu-id="e4b2b-213">15034</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-214">Ресурс слишком старый, чтобы быть совместимым.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-214">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-215"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**\_ \_ \_ слишком \_ Новая версия ошибки evt**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-215"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-216">15035</span><span class="sxs-lookup"><span data-stu-id="e4b2b-216">15035</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-217">Ресурс слишком новый для совместимости.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-217">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-218"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**Ошибка \_ evt \_ не \_ удается \_ открыть \_ канал \_ запроса**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-218"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-219">15036</span><span class="sxs-lookup"><span data-stu-id="e4b2b-219">15036</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-220">Невозможно открыть канал по указанному индексу запроса.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-220">The channel at the specified index of the query cannot be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-221"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**Ошибка \_ " \_ Издатель evt \_ отключен"**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-221"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-222">15037</span><span class="sxs-lookup"><span data-stu-id="e4b2b-222">15037</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-223">Поставщик отключен, и его ресурсы недоступны.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-223">The provider has been disabled and its resources are not available.</span></span> <span data-ttu-id="e4b2b-224">Это может произойти при удалении или обновлении поставщика.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-224">This can occur when the provider is uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4b2b-225"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ОШИБОЧный \_ \_ Фильтр evt \_ за пределами \_ \_ диапазона**</span><span class="sxs-lookup"><span data-stu-id="e4b2b-225"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4b2b-226">15038</span><span class="sxs-lookup"><span data-stu-id="e4b2b-226">15038</span></span>
</dt> <dt>



<span data-ttu-id="e4b2b-227">Попытка создать числовой тип, который находится за пределами допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="e4b2b-227">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4b2b-228">Требования</span><span class="sxs-lookup"><span data-stu-id="e4b2b-228">Requirements</span></span>



| <span data-ttu-id="e4b2b-229">Требование</span><span class="sxs-lookup"><span data-stu-id="e4b2b-229">Requirement</span></span> | <span data-ttu-id="e4b2b-230">Значение</span><span class="sxs-lookup"><span data-stu-id="e4b2b-230">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b2b-231">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4b2b-231">Minimum supported client</span></span><br/> | <span data-ttu-id="e4b2b-232">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4b2b-232">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4b2b-233">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4b2b-233">Minimum supported server</span></span><br/> | <span data-ttu-id="e4b2b-234">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4b2b-234">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4b2b-235">Header</span><span class="sxs-lookup"><span data-stu-id="e4b2b-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4b2b-236"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b2b-236"><dt>WinError.h</dt></span></span> </dl> |



 

 





