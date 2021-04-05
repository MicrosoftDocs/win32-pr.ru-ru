---
description: Отключает преобразование частоты кадров в MFT обработчика видео.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Атрибут MF_XVP_DISABLE_FRC (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991329"
---
# <a name="mf_xvp_disable_frc-attribute"></a><span data-ttu-id="d055c-103">MF \_ ксвп \_ Отключить \_ атрибут ФРК</span><span class="sxs-lookup"><span data-stu-id="d055c-103">MF\_XVP\_DISABLE\_FRC attribute</span></span>

<span data-ttu-id="d055c-104">Отключает преобразование частоты кадров в [**MFT обработчика видео**](video-processor-mft.md).</span><span class="sxs-lookup"><span data-stu-id="d055c-104">Disables frame-rate conversion in the [**Video Processor MFT**](video-processor-mft.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="d055c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d055c-105">Data type</span></span>

<span data-ttu-id="d055c-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="d055c-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d055c-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d055c-107">Remarks</span></span>

<span data-ttu-id="d055c-108">Если этот атрибут имеет **значение true**, обработчик видео не будет выполнять преобразование кадров.</span><span class="sxs-lookup"><span data-stu-id="d055c-108">If this attribute is **TRUE**, the video processor will not perform frame-rate conversion.</span></span> <span data-ttu-id="d055c-109">По умолчанию обработчик видео преобразует частоту кадров в соответствии с выходным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="d055c-109">By default, the video processor will convert the frame rate to match the output media type.</span></span>

<span data-ttu-id="d055c-110">Чтобы задать этот атрибут, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="d055c-110">To set this attribute:</span></span>

1.  <span data-ttu-id="d055c-111">Вызовите [**имфтрансформ:: OutAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) в обработчике видео.</span><span class="sxs-lookup"><span data-stu-id="d055c-111">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the video processor.</span></span>
2.  <span data-ttu-id="d055c-112">Вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d055c-112">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="d055c-113">Задайте атрибут перед началом потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="d055c-113">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="d055c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d055c-114">Requirements</span></span>



| <span data-ttu-id="d055c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d055c-115">Requirement</span></span> | <span data-ttu-id="d055c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d055c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d055c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d055c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d055c-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d055c-118">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d055c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d055c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d055c-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d055c-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d055c-121">Header</span><span class="sxs-lookup"><span data-stu-id="d055c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d055c-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d055c-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d055c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d055c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d055c-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d055c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




