---
description: Указывает, поврежден ли кадр видео.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: Атрибут MFSampleExtension_FrameCorruption (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155963"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="d1b80-103">Мфсампликстенсион \_ фрамекорруптион, атрибут</span><span class="sxs-lookup"><span data-stu-id="d1b80-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="d1b80-104">Указывает, поврежден ли кадр видео.</span><span class="sxs-lookup"><span data-stu-id="d1b80-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="d1b80-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d1b80-105">Data type</span></span>

<span data-ttu-id="d1b80-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d1b80-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d1b80-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="d1b80-107">Get/set</span></span>

<span data-ttu-id="d1b80-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d1b80-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d1b80-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d1b80-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d1b80-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="d1b80-110">Applies to</span></span>

[<span data-ttu-id="d1b80-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="d1b80-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="d1b80-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1b80-112">Remarks</span></span>

<span data-ttu-id="d1b80-113">Видеодекодер может установить этот атрибут для выходных образцов.</span><span class="sxs-lookup"><span data-stu-id="d1b80-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="d1b80-114">Если значение равно 1, декодер обнаружил повреждение данных в кадре.</span><span class="sxs-lookup"><span data-stu-id="d1b80-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="d1b80-115">Если значение равно 0, данные не повреждены или ничего не обнаружено.</span><span class="sxs-lookup"><span data-stu-id="d1b80-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b80-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d1b80-116">Requirements</span></span>



| <span data-ttu-id="d1b80-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d1b80-117">Requirement</span></span> | <span data-ttu-id="d1b80-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b80-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b80-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1b80-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b80-120">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1b80-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="d1b80-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1b80-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b80-122">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d1b80-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d1b80-123">Header</span><span class="sxs-lookup"><span data-stu-id="d1b80-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1b80-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1b80-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b80-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1b80-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b80-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1b80-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1b80-127">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="d1b80-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="d1b80-128">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="d1b80-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




