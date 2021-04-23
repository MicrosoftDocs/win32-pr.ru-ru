---
description: Атрибут, который передается в Имфмедиаенгиненидкэйнотифи механизму мультимедиа при создании.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: Атрибут MF_MEDIA_ENGINE_NEEDKEY_CALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693870"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="7697f-103">\_ \_ \_ Атрибут обратного вызова нидкэй для механизма передачи мультимедиа MF \_</span><span class="sxs-lookup"><span data-stu-id="7697f-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="7697f-104">Атрибут, который передается в [**имфмедиаенгиненидкэйнотифи**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) механизму мультимедиа при создании.</span><span class="sxs-lookup"><span data-stu-id="7697f-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="7697f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7697f-105">Data type</span></span>

<span data-ttu-id="7697f-106">**Имфмедиаенгиненидкэйнотифи \* *_ хранится как _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="7697f-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="7697f-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="7697f-107">Get/set</span></span>

<span data-ttu-id="7697f-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="7697f-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="7697f-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="7697f-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="7697f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7697f-110">Remarks</span></span>

<span data-ttu-id="7697f-111">Значением этого атрибута является указатель на интерфейс [**имфмедиаенгиненидкэйнотифи**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , реализованный приложением.</span><span class="sxs-lookup"><span data-stu-id="7697f-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="7697f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="7697f-112">Requirements</span></span>



| <span data-ttu-id="7697f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="7697f-113">Requirement</span></span> | <span data-ttu-id="7697f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7697f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7697f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7697f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7697f-116">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7697f-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7697f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7697f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7697f-118">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7697f-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7697f-119">IDL</span><span class="sxs-lookup"><span data-stu-id="7697f-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7697f-120"><dt>Мфмедиаенгине. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7697f-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7697f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7697f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7697f-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7697f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




