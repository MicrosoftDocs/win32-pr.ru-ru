---
description: Задает промежуточную ширину кадра для кодированного видео.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: Свойство MFPKEY_FORCEFRAMEWIDTH (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea4c8c7ac025de1c089c592a591136df966797d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544919"
---
# <a name="mfpkey_forceframewidth-property"></a><span data-ttu-id="1757f-103">МФПКЭЙ \_ форцефрамевидс, свойство</span><span class="sxs-lookup"><span data-stu-id="1757f-103">MFPKEY\_FORCEFRAMEWIDTH Property</span></span>

<span data-ttu-id="1757f-104">Задает промежуточную ширину кадра для кодированного видео.</span><span class="sxs-lookup"><span data-stu-id="1757f-104">Specifies an intermediate frame width for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1757f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1757f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1757f-106">g \_ всзвмвкфорцефрамевидс</span><span class="sxs-lookup"><span data-stu-id="1757f-106">g\_wszWMVCForceFrameWidth</span></span>

## <a name="data-type"></a><span data-ttu-id="1757f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1757f-107">Data Type</span></span>

<span data-ttu-id="1757f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1757f-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="1757f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1757f-109">Remarks</span></span>

<span data-ttu-id="1757f-110">Вы можете задать это значение и свойство [мфпкэй \_ форцефрамехеигхт](mfpkey-forceframeheightproperty.md) , чтобы заставить кодировщик кодировать видеопоток размером кадра, размер которого меньше, чем размер кадра ввода или вывода.</span><span class="sxs-lookup"><span data-stu-id="1757f-110">You can set this value and the [MFPKEY\_FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="1757f-111">При декодировании видео будет изменено до исходного разрешения ввода.</span><span class="sxs-lookup"><span data-stu-id="1757f-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="1757f-112">Допустимые размеры рамки на любой из осей — от 2 до 8192 пикселей.</span><span class="sxs-lookup"><span data-stu-id="1757f-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="1757f-113">Размеры фрейма должны быть кратны 2.</span><span class="sxs-lookup"><span data-stu-id="1757f-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="1757f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1757f-114">Requirements</span></span>



| <span data-ttu-id="1757f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1757f-115">Requirement</span></span> | <span data-ttu-id="1757f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1757f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1757f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1757f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1757f-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1757f-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1757f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1757f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1757f-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1757f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1757f-121">Header</span><span class="sxs-lookup"><span data-stu-id="1757f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1757f-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1757f-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1757f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1757f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1757f-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1757f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




