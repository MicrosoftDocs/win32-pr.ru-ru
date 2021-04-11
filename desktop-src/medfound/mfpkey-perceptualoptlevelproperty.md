---
description: Указывает, должен ли кодек использовать консервативную оптимизацию искусственного при кодировании.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Свойство MFPKEY_PERCEPTUALOPTLEVEL (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263983"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="71ea1-103">МФПКЭЙ \_ перцептуалоптлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="71ea1-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="71ea1-104">Указывает, должен ли кодек использовать консервативную оптимизацию искусственного при кодировании.</span><span class="sxs-lookup"><span data-stu-id="71ea1-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="71ea1-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="71ea1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="71ea1-106">g \_ всзвмвкперцептуалоптлевел</span><span class="sxs-lookup"><span data-stu-id="71ea1-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="71ea1-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="71ea1-107">Data Type</span></span>

<span data-ttu-id="71ea1-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="71ea1-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="71ea1-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="71ea1-109">Default Value</span></span>

<span data-ttu-id="71ea1-110">0</span><span class="sxs-lookup"><span data-stu-id="71ea1-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="71ea1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71ea1-111">Remarks</span></span>

<span data-ttu-id="71ea1-112">Консервативная оптимизация искусственного — это процесс, с помощью которого кодек пытается выделить "важные" и "неважные" регионы в видеокадре.</span><span class="sxs-lookup"><span data-stu-id="71ea1-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="71ea1-113">Определив эти регионы кадра, кодек предоставит более высокий приоритет для важных регионов, за счет чего качество неважных регионов.</span><span class="sxs-lookup"><span data-stu-id="71ea1-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="71ea1-114">Искусственного оптимизация позволяет подчеркнуть, что изображение отображается правильно для человеческого глаза, а не накладывается на более математическую точность.</span><span class="sxs-lookup"><span data-stu-id="71ea1-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="71ea1-115">Результаты оптимизации будут зависеть от типа закодированного видео.</span><span class="sxs-lookup"><span data-stu-id="71ea1-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="71ea1-116">Эта функция может быть хорошо подходит для кодирования с низкими и низким уровнем разрешений (например, веб-потоковой передачи), но ее, возможно, следует избегать, когда надежде для архивирования качества видео.</span><span class="sxs-lookup"><span data-stu-id="71ea1-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ea1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="71ea1-117">Requirements</span></span>



| <span data-ttu-id="71ea1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="71ea1-118">Requirement</span></span> | <span data-ttu-id="71ea1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="71ea1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71ea1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71ea1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71ea1-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="71ea1-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="71ea1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71ea1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71ea1-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71ea1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="71ea1-124">Header</span><span class="sxs-lookup"><span data-stu-id="71ea1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ea1-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ea1-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ea1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71ea1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ea1-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="71ea1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




