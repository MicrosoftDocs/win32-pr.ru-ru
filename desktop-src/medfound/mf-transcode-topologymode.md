---
description: Указывает для топологии кодирования, будет ли загрузчик топологии загружать преобразования на основе оборудования.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Атрибут MF_TRANSCODE_TOPOLOGYMODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897938"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="b79cb-103">\_Атрибут топологимоде для ПЕРЕКОДИРОВАНИЯ MF \_</span><span class="sxs-lookup"><span data-stu-id="b79cb-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="b79cb-104">Указывает для топологии кодирования, будет ли загрузчик топологии загружать преобразования на основе оборудования.</span><span class="sxs-lookup"><span data-stu-id="b79cb-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="b79cb-105">Режим топологии указывает, можно ли использовать аппаратные преобразования (например, аппаратные кодеки) в топологии перекодирования.</span><span class="sxs-lookup"><span data-stu-id="b79cb-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="b79cb-106">Приложение может сохранить этот атрибут в профиле перекодирования путем вызова [**имфтранскодепрофиле:: сетконтаинераттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="b79cb-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="b79cb-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b79cb-107">Data type</span></span>

<span data-ttu-id="b79cb-108">**[**MF \_ Перекодировать \_ \_ Флаги топологимоде**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** , хранящиеся в виде **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b79cb-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b79cb-109">Get/Set</span><span class="sxs-lookup"><span data-stu-id="b79cb-109">Get/set</span></span>

<span data-ttu-id="b79cb-110">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b79cb-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b79cb-111">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b79cb-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b79cb-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b79cb-112">Remarks</span></span>

<span data-ttu-id="b79cb-113">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b79cb-113">This attribute is optional.</span></span> <span data-ttu-id="b79cb-114">Он должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b79cb-114">It must have one of the following values.</span></span>



| <span data-ttu-id="b79cb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b79cb-115">Value</span></span>                                              | <span data-ttu-id="b79cb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b79cb-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b79cb-117">**топологимоде (MF), \_ \_ \_ \_ разрешенное оборудование**</span><span class="sxs-lookup"><span data-stu-id="b79cb-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="b79cb-118">Загрузчик топологии будет загружать аппаратные МФТС, такие как аппаратные декодеры, если они доступны.</span><span class="sxs-lookup"><span data-stu-id="b79cb-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="b79cb-119">Загрузчик топологии автоматически возвращается к программному декодированию, если аппаратный декодер не найден или если аппаратный декодер не может подключиться по какой-либо причине.</span><span class="sxs-lookup"><span data-stu-id="b79cb-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="b79cb-120">**MF \_ перекодировать \_ \_ только программное обеспечение топологимоде \_**</span><span class="sxs-lookup"><span data-stu-id="b79cb-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="b79cb-121">Загрузчик топологии будет загружать только МФТС программного обеспечения, включая программные декодеры.</span><span class="sxs-lookup"><span data-stu-id="b79cb-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="b79cb-122">Значение по умолчанию — **MF \_ \_ топологимоде \_ Software \_**.</span><span class="sxs-lookup"><span data-stu-id="b79cb-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="b79cb-123">Если загрузчик топологии вставляет в топологию основную таблицу оборудования, в узле Topology задается атрибут [ \_ \_ \_ \_ атрибута «URL-адрес перечисления MFT](mft-enum-hardware-url-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="b79cb-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="b79cb-124">Чтобы проверить наличие в файле MFT оборудования, перечислите узлы в разрешенной топологии и проверьте наличие этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="b79cb-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="b79cb-125">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b79cb-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79cb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b79cb-126">Requirements</span></span>



| <span data-ttu-id="b79cb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b79cb-127">Requirement</span></span> | <span data-ttu-id="b79cb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b79cb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b79cb-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b79cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b79cb-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b79cb-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b79cb-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b79cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b79cb-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b79cb-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b79cb-133">Header</span><span class="sxs-lookup"><span data-stu-id="b79cb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b79cb-134"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b79cb-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79cb-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b79cb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79cb-136">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b79cb-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b79cb-137">API перекодирования</span><span class="sxs-lookup"><span data-stu-id="b79cb-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="b79cb-138">**Имфтранскодепрофиле:: Жетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="b79cb-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="b79cb-139">**Имфтранскодепрофиле:: Сетконтаинераттрибутес**</span><span class="sxs-lookup"><span data-stu-id="b79cb-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




