---
description: Указывает, содержит ли образец носителя трехмерный видеокадр.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Атрибут MFSampleExtension_3DVideo (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701807"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="be049-103">Мфсампликстенсион \_ 3DVideo, атрибут</span><span class="sxs-lookup"><span data-stu-id="be049-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="be049-104">Указывает, содержит ли образец носителя трехмерный видеокадр.</span><span class="sxs-lookup"><span data-stu-id="be049-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="be049-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="be049-105">Data type</span></span>

<span data-ttu-id="be049-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="be049-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="be049-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be049-107">Remarks</span></span>

<span data-ttu-id="be049-108">Если этот атрибут имеет **значение true**, пример носителя содержит видеокадр с двумя или более стереоскопик представлениями.</span><span class="sxs-lookup"><span data-stu-id="be049-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="be049-109">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="be049-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="be049-110">Компонент, создающий трехмерные видеокадры, должен установить для этого атрибута **значение true** на каждом образце носителя, содержащем трехмерный кадр.</span><span class="sxs-lookup"><span data-stu-id="be049-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="be049-111">Требования</span><span class="sxs-lookup"><span data-stu-id="be049-111">Requirements</span></span>



| <span data-ttu-id="be049-112">Требование</span><span class="sxs-lookup"><span data-stu-id="be049-112">Requirement</span></span> | <span data-ttu-id="be049-113">Значение</span><span class="sxs-lookup"><span data-stu-id="be049-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be049-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be049-114">Minimum supported client</span></span><br/> | <span data-ttu-id="be049-115">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="be049-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="be049-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be049-116">Minimum supported server</span></span><br/> | <span data-ttu-id="be049-117">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="be049-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="be049-118">Header</span><span class="sxs-lookup"><span data-stu-id="be049-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="be049-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="be049-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be049-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be049-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be049-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="be049-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="be049-122">Мфсампликстенсион \_ 3DVideo \_ самплеформат</span><span class="sxs-lookup"><span data-stu-id="be049-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




