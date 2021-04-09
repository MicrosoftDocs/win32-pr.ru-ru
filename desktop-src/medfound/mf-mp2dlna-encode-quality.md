---
description: Указывает качество кодирования для приемника мультимедиа Digital живая Network Alliance (DLNA).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Атрибут MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080870"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="2e994-103">\_ \_ Атрибут качества шифрования MF MP2DLNA \_</span><span class="sxs-lookup"><span data-stu-id="2e994-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="2e994-104">Указывает качество кодирования для приемника мультимедиа Digital живая Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="2e994-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="2e994-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2e994-105">Data type</span></span>

<span data-ttu-id="2e994-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2e994-106">**UINT32**</span></span>

<span data-ttu-id="2e994-107">Диапазон: 0 – 18</span><span class="sxs-lookup"><span data-stu-id="2e994-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="2e994-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="2e994-108">Get/set</span></span>

<span data-ttu-id="2e994-109">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="2e994-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="2e994-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="2e994-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="2e994-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e994-111">Remarks</span></span>

<span data-ttu-id="2e994-112">Большее число указывает на лучшее качество кодирования.</span><span class="sxs-lookup"><span data-stu-id="2e994-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="2e994-113">Меньшие числа указывают на ускорение кодирования, но с более низким качеством кодирования.</span><span class="sxs-lookup"><span data-stu-id="2e994-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="2e994-114">Значение по умолчанию — 9.</span><span class="sxs-lookup"><span data-stu-id="2e994-114">The default value is 9.</span></span>

<span data-ttu-id="2e994-115">Чтобы задать этот атрибут для приемника мультимедиа DLNA, запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="2e994-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="2e994-116">Задайте атрибут перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="2e994-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e994-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2e994-117">Requirements</span></span>



| <span data-ttu-id="2e994-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2e994-118">Requirement</span></span> | <span data-ttu-id="2e994-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2e994-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e994-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e994-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e994-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2e994-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e994-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e994-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e994-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e994-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2e994-124">Header</span><span class="sxs-lookup"><span data-stu-id="2e994-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e994-125"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e994-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e994-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e994-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e994-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e994-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




