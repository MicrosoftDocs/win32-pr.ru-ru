---
description: Следующие подтипы используются декодерами, использующими ускорение видео DirectX (ДКСВА).
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: Подтипы видео по ускорению DirectX видео (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0df0f079e795638c6802570c95e2468209a7256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675582"
---
# <a name="directx-video-acceleration-video-subtypes"></a><span data-ttu-id="07ac5-103">Подтипы видео для ускорения видео DirectX</span><span class="sxs-lookup"><span data-stu-id="07ac5-103">DirectX Video Acceleration Video Subtypes</span></span>

<span data-ttu-id="07ac5-104">Следующие подтипы используются декодерами, использующими ускорение видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="07ac5-104">The following subtypes are used by decoders that are using DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="07ac5-105">AI44 и IA44 — это поверхности с числом бит на пиксель, равное 8.</span><span class="sxs-lookup"><span data-stu-id="07ac5-105">AI44 and IA44 are surfaces with a bits-per-pixel value of 8.</span></span> <span data-ttu-id="07ac5-106">Существует 4 бита I и 4 *бита.* *Я* представляет индекс в 16-входной палитре YUV.</span><span class="sxs-lookup"><span data-stu-id="07ac5-106">There are 4 bits of I and 4 bits of *A*. *I* represents an index into a 16-entry YUV palette.</span></span> <span data-ttu-id="07ac5-107">*Представляет 4* бита информации о прозрачности (также известной как «на пиксель-альфа»).</span><span class="sxs-lookup"><span data-stu-id="07ac5-107">*A* represents 4 bits of transparency information (also known as per-pixel-alpha).</span></span> <span data-ttu-id="07ac5-108">Таким образом, поверхности AI44 и IA44 позволяют использовать 16 различных цветов в 16 различных значениях прозрачности или 256 различных представлениях пикселей.</span><span class="sxs-lookup"><span data-stu-id="07ac5-108">Therefore, AI44 and IA44 surfaces allow for 16 different colors at 16 different transparency values, or 256 different pixel representations.</span></span> <span data-ttu-id="07ac5-109">При использовании AI44 альфа-канал сохраняется в самом старшем, в IA44 альфа-канал сохраняется в пошаговом процессе.</span><span class="sxs-lookup"><span data-stu-id="07ac5-109">With AI44 the alpha is stored in the hi-nibble, in IA44 the alpha is stored in the lo-nibble.</span></span> <span data-ttu-id="07ac5-110">Оба формата очень полезны для изображений с подизображением DVD, Line21 и телетекста.</span><span class="sxs-lookup"><span data-stu-id="07ac5-110">Both formats are very useful for DVD sub-picture images and Line21 and Teletext images.</span></span> <span data-ttu-id="07ac5-111">Корпорация Майкрософт предпочитает версию AI44, поскольку она немного упрощает создание текста с использованием этого формата.</span><span class="sxs-lookup"><span data-stu-id="07ac5-111">Microsoft prefers the AI44 version because it is slightly easier to generate text using this format.</span></span>

| <span data-ttu-id="07ac5-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="07ac5-112">Subtype</span></span>            | <span data-ttu-id="07ac5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="07ac5-113">Description</span></span>                                                 |
|--------------------|-------------------------------------------------------------|
| <span data-ttu-id="07ac5-114">МЕДИАСУБТИПЕ \_ AI44</span><span class="sxs-lookup"><span data-stu-id="07ac5-114">MEDIASUBTYPE\_AI44</span></span> | <span data-ttu-id="07ac5-115">Для подизображения и наложения текста.</span><span class="sxs-lookup"><span data-stu-id="07ac5-115">For subpicture and text overlays.</span></span> <span data-ttu-id="07ac5-116">См. предыдущее описание.</span><span class="sxs-lookup"><span data-stu-id="07ac5-116">See previous description.</span></span> |
| <span data-ttu-id="07ac5-117">МЕДИАСУБТИПЕ \_ IA44</span><span class="sxs-lookup"><span data-stu-id="07ac5-117">MEDIASUBTYPE\_IA44</span></span> | <span data-ttu-id="07ac5-118">Для подизображения и наложения текста.</span><span class="sxs-lookup"><span data-stu-id="07ac5-118">For subpicture and text overlays.</span></span> <span data-ttu-id="07ac5-119">См. предыдущее описание.</span><span class="sxs-lookup"><span data-stu-id="07ac5-119">See previous description.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="07ac5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="07ac5-120">Requirements</span></span>



| <span data-ttu-id="07ac5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="07ac5-121">Requirement</span></span> | <span data-ttu-id="07ac5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="07ac5-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07ac5-123">Header</span><span class="sxs-lookup"><span data-stu-id="07ac5-123">Header</span></span><br/> | <dl> <span data-ttu-id="07ac5-124"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="07ac5-124"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07ac5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07ac5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ac5-126">Подтипы видео</span><span class="sxs-lookup"><span data-stu-id="07ac5-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> </dl>

 

 




