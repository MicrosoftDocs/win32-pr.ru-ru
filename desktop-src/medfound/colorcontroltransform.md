---
description: Регулирует цветовые характеристики потока видео.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: Преобразование элемента управления цветом DSP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b94c8314bfd2be85a3bbc392bfa0e83767ff0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808159"
---
# <a name="color-control-transform-dsp"></a><span data-ttu-id="90fc4-103">Преобразование элемента управления цветом DSP</span><span class="sxs-lookup"><span data-stu-id="90fc4-103">Color Control Transform DSP</span></span>

<span data-ttu-id="90fc4-104">Регулирует цветовые характеристики потока видео.</span><span class="sxs-lookup"><span data-stu-id="90fc4-104">Adjusts the color characteristics of a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="90fc4-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="90fc4-105">CLSID</span></span>

<span data-ttu-id="90fc4-106">\_ККОЛОРКОНТРОЛДМО CLSID</span><span class="sxs-lookup"><span data-stu-id="90fc4-106">CLSID\_CColorControlDmo</span></span>

## <a name="interfaces"></a><span data-ttu-id="90fc4-107">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="90fc4-107">Interfaces</span></span>

-   <span data-ttu-id="90fc4-108">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="90fc4-108">**IMediaObject**</span></span>
-   <span data-ttu-id="90fc4-109">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="90fc4-109">**IMFTransform**</span></span>
-   <span data-ttu-id="90fc4-110">**ипропертисторе**</span><span class="sxs-lookup"><span data-stu-id="90fc4-110">**IPropertyStore**</span></span>

## <a name="formats"></a><span data-ttu-id="90fc4-111">Форматы</span><span class="sxs-lookup"><span data-stu-id="90fc4-111">Formats</span></span>

-   <span data-ttu-id="90fc4-112">RGB 24</span><span class="sxs-lookup"><span data-stu-id="90fc4-112">RGB 24</span></span>
-   <span data-ttu-id="90fc4-113">RGB 32</span><span class="sxs-lookup"><span data-stu-id="90fc4-113">RGB 32</span></span>
-   <span data-ttu-id="90fc4-114">RGB 555</span><span class="sxs-lookup"><span data-stu-id="90fc4-114">RGB 555</span></span>
-   <span data-ttu-id="90fc4-115">RGB 565</span><span class="sxs-lookup"><span data-stu-id="90fc4-115">RGB 565</span></span>
-   <span data-ttu-id="90fc4-116">айув</span><span class="sxs-lookup"><span data-stu-id="90fc4-116">AYUV</span></span>
-   <span data-ttu-id="90fc4-117">UYVY</span><span class="sxs-lookup"><span data-stu-id="90fc4-117">UYVY</span></span>
-   <span data-ttu-id="90fc4-118">YUY2</span><span class="sxs-lookup"><span data-stu-id="90fc4-118">YUY2</span></span>
-   <span data-ttu-id="90fc4-119">YV12</span><span class="sxs-lookup"><span data-stu-id="90fc4-119">YV12</span></span>

## <a name="properties"></a><span data-ttu-id="90fc4-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="90fc4-120">Properties</span></span>

-   [<span data-ttu-id="90fc4-121">\_цветовая \_ яркость мфпкэй</span><span class="sxs-lookup"><span data-stu-id="90fc4-121">MFPKEY\_COLOR\_BRIGHTNESS</span></span>](mfpkey-color-brightness.md)
-   [<span data-ttu-id="90fc4-122">\_ \_ контрастность цвета мфпкэй</span><span class="sxs-lookup"><span data-stu-id="90fc4-122">MFPKEY\_COLOR\_CONTRAST</span></span>](mfpkey-color-contrast.md)
-   [<span data-ttu-id="90fc4-123">\_цветовой \_ тон мфпкэй</span><span class="sxs-lookup"><span data-stu-id="90fc4-123">MFPKEY\_COLOR\_HUE</span></span>](mfpkey-color-hue.md)
-   [<span data-ttu-id="90fc4-124">МФПКЭЙ \_ \_ насыщенность цвета</span><span class="sxs-lookup"><span data-stu-id="90fc4-124">MFPKEY\_COLOR\_SATURATION</span></span>](mfpkey-color-saturation.md)

## <a name="remarks"></a><span data-ttu-id="90fc4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90fc4-125">Remarks</span></span>

<span data-ttu-id="90fc4-126">Этот DSP изменяет содержимое потока видео.</span><span class="sxs-lookup"><span data-stu-id="90fc4-126">This DSP modifies the contents of the video stream.</span></span> <span data-ttu-id="90fc4-127">Для воспроизведения можно повысить эффективность аналогичных эффектов с помощью интерфейса **имфвидеопроцессор** , который управляет обработкой видео в графической карте.</span><span class="sxs-lookup"><span data-stu-id="90fc4-127">For playback, you might be able to achieve similar effects more efficiently by using the **IMFVideoProcessor** interface, which controls video processing in the graphics card.</span></span>

## <a name="requirements"></a><span data-ttu-id="90fc4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="90fc4-128">Requirements</span></span>



| <span data-ttu-id="90fc4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="90fc4-129">Requirement</span></span> | <span data-ttu-id="90fc4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="90fc4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90fc4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90fc4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="90fc4-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90fc4-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="90fc4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90fc4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="90fc4-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90fc4-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90fc4-135">Header</span><span class="sxs-lookup"><span data-stu-id="90fc4-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="90fc4-136"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="90fc4-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="90fc4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="90fc4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90fc4-138"><dt>Mfvdsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90fc4-138"><dt>Mfvdsp.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90fc4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90fc4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90fc4-140">Обработчики цифровых сигналов</span><span class="sxs-lookup"><span data-stu-id="90fc4-140">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




