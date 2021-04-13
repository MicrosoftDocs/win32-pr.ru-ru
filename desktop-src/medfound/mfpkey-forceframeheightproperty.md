---
description: Задает промежуточную высоту кадра для кодированного видео.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: Свойство MFPKEY_FORCEFRAMEHEIGHT (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263994"
---
# <a name="mfpkey_forceframeheight-property"></a><span data-ttu-id="7bf76-103">МФПКЭЙ \_ форцефрамехеигхт, свойство</span><span class="sxs-lookup"><span data-stu-id="7bf76-103">MFPKEY\_FORCEFRAMEHEIGHT Property</span></span>

<span data-ttu-id="7bf76-104">Задает промежуточную высоту кадра для кодированного видео.</span><span class="sxs-lookup"><span data-stu-id="7bf76-104">Specifies an intermediate frame height for encoded video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7bf76-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="7bf76-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7bf76-106">g \_ всзвмвкфорцефрамехеигхт</span><span class="sxs-lookup"><span data-stu-id="7bf76-106">g\_wszWMVCForceFrameHeight</span></span>

## <a name="data-type"></a><span data-ttu-id="7bf76-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7bf76-107">Data Type</span></span>

<span data-ttu-id="7bf76-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7bf76-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf76-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bf76-109">Remarks</span></span>

<span data-ttu-id="7bf76-110">Вы можете задать это значение и свойство [мфпкэй \_ форцефрамевидс](mfpkey-forceframewidthproperty.md) , чтобы заставить кодировщик кодировать видеопоток размером кадра, размер которого меньше, чем размер кадра ввода или вывода.</span><span class="sxs-lookup"><span data-stu-id="7bf76-110">You can set this value and the [MFPKEY\_FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) property to force the encoder to encode the video stream with a frame size that is smaller than the input or output frame sizes.</span></span> <span data-ttu-id="7bf76-111">При декодировании видео будет изменено до исходного разрешения ввода.</span><span class="sxs-lookup"><span data-stu-id="7bf76-111">When decoded, the video will be resized to its original input resolution.</span></span>

<span data-ttu-id="7bf76-112">Допустимые размеры рамки на любой из осей — от 2 до 8192 пикселей.</span><span class="sxs-lookup"><span data-stu-id="7bf76-112">Valid frame dimensions on either axis are 2 to 8192 pixels.</span></span> <span data-ttu-id="7bf76-113">Размеры фрейма должны быть кратны 2.</span><span class="sxs-lookup"><span data-stu-id="7bf76-113">Frame dimensions must be divisible by 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf76-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7bf76-114">Requirements</span></span>



| <span data-ttu-id="7bf76-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7bf76-115">Requirement</span></span> | <span data-ttu-id="7bf76-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7bf76-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf76-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7bf76-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf76-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7bf76-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7bf76-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7bf76-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf76-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7bf76-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7bf76-121">Header</span><span class="sxs-lookup"><span data-stu-id="7bf76-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf76-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bf76-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf76-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bf76-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf76-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7bf76-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




