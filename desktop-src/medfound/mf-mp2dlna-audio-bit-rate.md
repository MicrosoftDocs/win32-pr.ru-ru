---
description: Указывает максимальную скорость потока звука для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: d0ae573a-7ce3-49e8-9609-f72d067f1ce1
title: Атрибут MF_MP2DLNA_AUDIO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c61554f592aefbb863057339d807e23fc96567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991477"
---
# <a name="mf_mp2dlna_audio_bit_rate-attribute"></a><span data-ttu-id="0f789-103">\_ \_ \_ Атрибут скорости звукового бита MP2DLNA \_ MF</span><span class="sxs-lookup"><span data-stu-id="0f789-103">MF\_MP2DLNA\_AUDIO\_BIT\_RATE attribute</span></span>

<span data-ttu-id="0f789-104">Указывает максимальную скорость потока звука для приемника мультимедиа Digital живая Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="0f789-104">Specifies the maximum audio bit rate for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="0f789-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0f789-105">Data type</span></span>

<span data-ttu-id="0f789-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0f789-106">**UINT32**</span></span>

<span data-ttu-id="0f789-107">Значение является целевой максимальной скоростью потока для закодированного аудиопотока в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="0f789-107">The value is the target maximum bit rate for the encoded audio stream, in bits per second.</span></span> <span data-ttu-id="0f789-108">Значение должно быть одной из битовых ставок, допустимых для звука MPEG-2 уровня 2 для DLNA.</span><span class="sxs-lookup"><span data-stu-id="0f789-108">The value must be one of the bit rates allowed for MPEG-2 layer 2 audio for DLNA.</span></span> <span data-ttu-id="0f789-109">Значение по умолчанию — 192000 (192 кбит/с).</span><span class="sxs-lookup"><span data-stu-id="0f789-109">The default value is 192000 (192 Kbps).</span></span>

## <a name="getset"></a><span data-ttu-id="0f789-110">Get/Set</span><span class="sxs-lookup"><span data-stu-id="0f789-110">Get/set</span></span>

<span data-ttu-id="0f789-111">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0f789-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0f789-112">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0f789-112">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f789-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f789-113">Remarks</span></span>

<span data-ttu-id="0f789-114">Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="0f789-114">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="0f789-115">Задайте атрибут перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0f789-115">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f789-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0f789-116">Requirements</span></span>



| <span data-ttu-id="0f789-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0f789-117">Requirement</span></span> | <span data-ttu-id="0f789-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0f789-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f789-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f789-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0f789-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0f789-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0f789-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f789-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0f789-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f789-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f789-123">Header</span><span class="sxs-lookup"><span data-stu-id="0f789-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f789-124"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f789-124"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f789-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f789-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f789-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f789-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




