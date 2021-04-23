---
description: Указывает, будет ли загрузчик топологии перечислять типы носителей, предоставляемые источником мультимедиа.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Атрибут MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343312"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="31aa6-103">\_ \_ Перечисление \_ типа источника для топологии \_ MF</span><span class="sxs-lookup"><span data-stu-id="31aa6-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="31aa6-104">Указывает, будет ли загрузчик топологии перечислять типы носителей, предоставляемые источником мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31aa6-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="31aa6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="31aa6-105">Data type</span></span>

<span data-ttu-id="31aa6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="31aa6-106">**UINT32**</span></span>

<span data-ttu-id="31aa6-107">Используйте одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="31aa6-107">Use one of the following values.</span></span>



| <span data-ttu-id="31aa6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="31aa6-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="31aa6-109">Значение</span><span class="sxs-lookup"><span data-stu-id="31aa6-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="31aa6-110"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="31aa6-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="31aa6-111">Не перечислите исходные типы носителей.</span><span class="sxs-lookup"><span data-stu-id="31aa6-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="31aa6-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="31aa6-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="31aa6-113">Перечисление исходных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="31aa6-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="31aa6-114">Get/Set</span><span class="sxs-lookup"><span data-stu-id="31aa6-114">Get/set</span></span>

<span data-ttu-id="31aa6-115">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="31aa6-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="31aa6-116">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="31aa6-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="31aa6-117">Применяется к</span><span class="sxs-lookup"><span data-stu-id="31aa6-117">Applies to</span></span>

[<span data-ttu-id="31aa6-118">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="31aa6-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="31aa6-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31aa6-119">Remarks</span></span>

<span data-ttu-id="31aa6-120">Каждый поток в источнике мультимедиа может предлагать более одного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31aa6-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="31aa6-121">Список типов перечисляется через интерфейс [**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) в дескрипторе потока.</span><span class="sxs-lookup"><span data-stu-id="31aa6-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="31aa6-122">Порядок, в котором загрузчик топологии пытается установить тип носителя источника мультимедиа, управляется двумя атрибутами:</span><span class="sxs-lookup"><span data-stu-id="31aa6-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="31aa6-123">\_Топология MF \_ Перечисление \_ исходных \_ типов в топологии.</span><span class="sxs-lookup"><span data-stu-id="31aa6-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="31aa6-124">Атрибут [**\_ \_ \_ метода соединения MF топоноде**](mf-toponode-connect-method-attribute.md) в исходном узле.</span><span class="sxs-lookup"><span data-stu-id="31aa6-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="31aa6-125">Если в качестве \_ значения \_ атрибута Source-Topology перечислить значение \_ \_ **false** или не задано, загрузчик топологии использует текущий тип носителя потока.</span><span class="sxs-lookup"><span data-stu-id="31aa6-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="31aa6-126">Он не перечисляет список возможных типов.</span><span class="sxs-lookup"><span data-stu-id="31aa6-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="31aa6-127">Если текущий тип мультимедиа несовместим с подчиненным узлом топологии и не удается найти сочетание декодеров и конвертеров, разрешение топологии завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="31aa6-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="31aa6-128">Если \_ \_ атрибуту MF Topology перечисление \_ \_ типов источника является **true**, загрузчик топологии перечисляет типы носителей источника до тех пор, пока не найдет совместимый тип.</span><span class="sxs-lookup"><span data-stu-id="31aa6-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="31aa6-129">В этом случае точный порядок операций зависит от того, содержит ли атрибут [**\_ \_ \_ метода топоноде Connect**](mf-toponode-connect-method-attribute.md) на исходном узле флаг **MF \_ Connect с \_ \_ независимым \_ свойств OutputTypes командлета** .</span><span class="sxs-lookup"><span data-stu-id="31aa6-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="31aa6-130">Если \_ \_ для параметра source Topology перечисление \_ типов источника задано \_ **значение true** и установлен флаг **MF \_ Connect \_ Resolve \_ независимый \_ свойств OutputTypes командлета** , то загрузчик топологии будет исчерпан каждый тип носителя перед переходом к следующему, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="31aa6-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="31aa6-131">Если \_ в ТОПОЛОГИИ MF \_ Перечисление \_ \_ типов источников имеет **значение true** , но **\_ Подключение MF Connect \_ \_ \_** не установлено, то загрузчик топологии пытается установить прямое соединение с каждым типом носителя, а затем пытается создать каждый тип мультимедиа с помощью преобразователей и, наконец, пытается создать каждый тип мультимедиа с помощью декодеров:</span><span class="sxs-lookup"><span data-stu-id="31aa6-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="31aa6-132">Если \_ в ТОПОЛОГИИ MF \_ Перечисление \_ \_ типов источников равно **false**, флаг **\_ \_ \_ независимого \_ свойств OutputTypes командлета для подключения MF** не учитывается.</span><span class="sxs-lookup"><span data-stu-id="31aa6-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="31aa6-133">\_ \_ \_ \_ Для совместимости с существующими приложениями значение по умолчанию, равное, имеет тип источника "ложь".</span><span class="sxs-lookup"><span data-stu-id="31aa6-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="31aa6-134">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="31aa6-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="31aa6-135">Пример</span><span class="sxs-lookup"><span data-stu-id="31aa6-135">Example</span></span>

<span data-ttu-id="31aa6-136">Ниже приведен пример, иллюстрирующий флаг **\_ \_ \_ независимого \_ свойств OutputTypes командлета для MF Connect** .</span><span class="sxs-lookup"><span data-stu-id="31aa6-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="31aa6-137">Предположим, что топология имеет \_ \_ для атрибута MF Topology перечисление \_ исходных типов значение \_ **true**.</span><span class="sxs-lookup"><span data-stu-id="31aa6-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="31aa6-138">Источник мультимедиа предлагает следующие типы:</span><span class="sxs-lookup"><span data-stu-id="31aa6-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="31aa6-139">T1, T2, T3</span><span class="sxs-lookup"><span data-stu-id="31aa6-139">T1, T2, T3</span></span>

<span data-ttu-id="31aa6-140">Приемник мультимедиа принимает следующие типы:</span><span class="sxs-lookup"><span data-stu-id="31aa6-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="31aa6-141">T3, T4</span><span class="sxs-lookup"><span data-stu-id="31aa6-141">T3, T4</span></span>

<span data-ttu-id="31aa6-142">Вариант 1. установлен флаг для **\_ \_ разрешения \_ независимых \_ свойств OutputTypes командлета MF Connect** .</span><span class="sxs-lookup"><span data-stu-id="31aa6-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="31aa6-143">Загрузчик топологии пытается установить прямое соединение с T1.</span><span class="sxs-lookup"><span data-stu-id="31aa6-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="31aa6-144">Приемник отклоняет T1.</span><span class="sxs-lookup"><span data-stu-id="31aa6-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="31aa6-145">Загрузчик топологии вставляет декодер, который принимает T1 и выводит T4.</span><span class="sxs-lookup"><span data-stu-id="31aa6-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="31aa6-146">Приемник принимает T4.</span><span class="sxs-lookup"><span data-stu-id="31aa6-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="31aa6-147">Окончательная топология содержит: источник мультимедиа → декодер > приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31aa6-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="31aa6-148">Вариант 2. флаг не задан.</span><span class="sxs-lookup"><span data-stu-id="31aa6-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="31aa6-149">Загрузчик топологии пытается установить прямое соединение с T1.</span><span class="sxs-lookup"><span data-stu-id="31aa6-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="31aa6-150">Приемник отклоняет T1.</span><span class="sxs-lookup"><span data-stu-id="31aa6-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="31aa6-151">Загрузчик топологии пытается выполнить прямое соединение с T2.</span><span class="sxs-lookup"><span data-stu-id="31aa6-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="31aa6-152">Приемник отклоняет T2.</span><span class="sxs-lookup"><span data-stu-id="31aa6-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="31aa6-153">Загрузчик топологии пытается установить прямое соединение с T3.</span><span class="sxs-lookup"><span data-stu-id="31aa6-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="31aa6-154">Приемник принимает T3.</span><span class="sxs-lookup"><span data-stu-id="31aa6-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="31aa6-155">Окончательная топология содержит: источник мультимедиа → приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="31aa6-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="31aa6-156">Требования</span><span class="sxs-lookup"><span data-stu-id="31aa6-156">Requirements</span></span>



| <span data-ttu-id="31aa6-157">Требование</span><span class="sxs-lookup"><span data-stu-id="31aa6-157">Requirement</span></span> | <span data-ttu-id="31aa6-158">Значение</span><span class="sxs-lookup"><span data-stu-id="31aa6-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31aa6-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31aa6-159">Minimum supported client</span></span><br/> | <span data-ttu-id="31aa6-160">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="31aa6-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="31aa6-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31aa6-161">Minimum supported server</span></span><br/> | <span data-ttu-id="31aa6-162">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="31aa6-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="31aa6-163">Header</span><span class="sxs-lookup"><span data-stu-id="31aa6-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="31aa6-164"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="31aa6-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31aa6-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31aa6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31aa6-166">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31aa6-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31aa6-167">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="31aa6-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




