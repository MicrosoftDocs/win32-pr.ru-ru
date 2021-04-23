---
description: Содержит внешние видеокамеры для образца.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: Атрибут MFSampleExtension_CameraExtrinsics (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662685"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="5bf0b-103">Мфсампликстенсион \_ камераекстринсикс, атрибут</span><span class="sxs-lookup"><span data-stu-id="5bf0b-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="5bf0b-104">Содержит внешние видеокамеры для образца.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5bf0b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5bf0b-105">Data type</span></span>

<span data-ttu-id="5bf0b-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="5bf0b-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="5bf0b-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="5bf0b-107">Get/set</span></span>

<span data-ttu-id="5bf0b-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="5bf0b-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5bf0b-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="5bf0b-110">Applies to</span></span>

[<span data-ttu-id="5bf0b-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="5bf0b-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="5bf0b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bf0b-112">Remarks</span></span>

<span data-ttu-id="5bf0b-113">Значением атрибута является [**мфкамераекстринсикс**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="5bf0b-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="5bf0b-114">Этот атрибут является необязательным для поддержки камер, которые не были откалиброваны.</span><span class="sxs-lookup"><span data-stu-id="5bf0b-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf0b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5bf0b-115">Requirements</span></span>



| <span data-ttu-id="5bf0b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5bf0b-116">Requirement</span></span> | <span data-ttu-id="5bf0b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5bf0b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf0b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5bf0b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5bf0b-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5bf0b-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5bf0b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5bf0b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5bf0b-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5bf0b-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5bf0b-122">Header</span><span class="sxs-lookup"><span data-stu-id="5bf0b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bf0b-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bf0b-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bf0b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5bf0b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf0b-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bf0b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




