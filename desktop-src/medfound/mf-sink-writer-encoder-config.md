---
description: Содержит указатель на хранилище свойств со свойствами кодировки.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: Атрибут MF_SINK_WRITER_ENCODER_CONFIG (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814889"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a><span data-ttu-id="186a2-103">\_ \_ \_ Атрибут конфигурации кодировщика записи MF SINK \_</span><span class="sxs-lookup"><span data-stu-id="186a2-103">MF\_SINK\_WRITER\_ENCODER\_CONFIG attribute</span></span>

<span data-ttu-id="186a2-104">Содержит указатель на хранилище свойств со свойствами кодировки.</span><span class="sxs-lookup"><span data-stu-id="186a2-104">Contains a pointer to a property store with encoding properties.</span></span>

## <a name="data-type"></a><span data-ttu-id="186a2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="186a2-105">Data type</span></span>

<span data-ttu-id="186a2-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="186a2-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="186a2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="186a2-107">Remarks</span></span>

<span data-ttu-id="186a2-108">Значением этого атрибута является указатель [_ *ипропертисторе* \*](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="186a2-108">The value of this attribute is an [_ *IPropertyStore*\*](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer.</span></span>

<span data-ttu-id="186a2-109">Этот атрибут позволяет приложению задавать свойства кодировки при использовании [модуля записи приемника](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="186a2-109">This attribute enables an application to set encoding properties when using the [Sink Writer](sink-writer.md).</span></span> <span data-ttu-id="186a2-110">Чтобы задать этот атрибут, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="186a2-110">To set this attribute, perform the following steps:</span></span>

1.  <span data-ttu-id="186a2-111">Вызовите [**пскреатемеморипропертисторе**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) , чтобы создать новое хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="186a2-111">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a new property store.</span></span>
2.  <span data-ttu-id="186a2-112">Задайте свойства кодировщика в хранилище свойств.</span><span class="sxs-lookup"><span data-stu-id="186a2-112">Set encoder properties on the property store.</span></span> <span data-ttu-id="186a2-113">Доступные свойства зависят от кодировщика.</span><span class="sxs-lookup"><span data-stu-id="186a2-113">The available properties depends on the encoder.</span></span> <span data-ttu-id="186a2-114">Дополнительные сведения см. в разделе [объекты кодека](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="186a2-114">For more information, see [Codec Objects](codecobjects.md).</span></span>
3.  <span data-ttu-id="186a2-115">Вызовите [**мфкреатеаттрибутес**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) , чтобы создать новое хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="186a2-115">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
4.  <span data-ttu-id="186a2-116">Вызовите метод [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) , чтобы задать указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в хранилище атрибутов.</span><span class="sxs-lookup"><span data-stu-id="186a2-116">Call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) to set the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer on the attribute store.</span></span>
5.  <span data-ttu-id="186a2-117">Создайте новый экземпляр модуля записи приемника.</span><span class="sxs-lookup"><span data-stu-id="186a2-117">Create a new instance of the Sink Writer.</span></span> <span data-ttu-id="186a2-118">Передайте указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) функции создания.</span><span class="sxs-lookup"><span data-stu-id="186a2-118">Pass the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer to the creation function.</span></span> <span data-ttu-id="186a2-119">Дополнительные сведения см. в разделе [атрибуты модуля записи приемника](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="186a2-119">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

<span data-ttu-id="186a2-120">Модуль записи приемника задает свойства кодировщика перед заданием типов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="186a2-120">The Sink Writer sets the properties on the encoder before setting the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="186a2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="186a2-121">Requirements</span></span>



| <span data-ttu-id="186a2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="186a2-122">Requirement</span></span> | <span data-ttu-id="186a2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="186a2-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="186a2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="186a2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="186a2-125">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="186a2-125">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="186a2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="186a2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="186a2-127">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="186a2-127">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="186a2-128">Header</span><span class="sxs-lookup"><span data-stu-id="186a2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="186a2-129"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="186a2-129"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="186a2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="186a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="186a2-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="186a2-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="186a2-132">**имфсинквритер**</span><span class="sxs-lookup"><span data-stu-id="186a2-132">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="186a2-133">Атрибуты модуля записи приемника</span><span class="sxs-lookup"><span data-stu-id="186a2-133">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 
