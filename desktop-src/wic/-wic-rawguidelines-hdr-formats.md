---
description: Форматы пикселей с высоким динамическим диапазоном
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Форматы пикселей с высоким динамическим диапазоном
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911940"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="903a8-103">Форматы пикселей с высоким динамическим диапазоном</span><span class="sxs-lookup"><span data-stu-id="903a8-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="903a8-104">Кодеки должны использовать форматы пикселей компонента Windows Imaging Component (WIC), сохраняющие весь динамический диапазон базовых данных датчика.</span><span class="sxs-lookup"><span data-stu-id="903a8-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="903a8-105">GUID \_ WICPixelFormat48bppRGB — это типичный формат 16-разрядного канала с фиксированной точкой, который можно использовать.</span><span class="sxs-lookup"><span data-stu-id="903a8-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="903a8-106">Также можно использовать и другие форматы с более высокой точностью.</span><span class="sxs-lookup"><span data-stu-id="903a8-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="903a8-107">Чтобы обеспечить полную поддержку конвейера отрисовки графического процессора (GPU) Windows Presentation Foundation, корпорация Майкрософт настоятельно рекомендует поддержку 32-разрядного формата пикселей с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="903a8-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="903a8-108">Форматы пикселей с высоким цветом. в Windows 7 добавлены два новых формата пикселей WIC для поддержки новых форматов дисплеев высокого цвета.</span><span class="sxs-lookup"><span data-stu-id="903a8-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="903a8-109">Это: GUID \_ WICPixelFormat32bppRGBA1010102 и GUID \_ WICPixelFormat32bppRGBA1010102XR.</span><span class="sxs-lookup"><span data-stu-id="903a8-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="903a8-110">Формат высокого цвета с 16 битами на канал (бит/с) поддерживается существующим \_ форматом GUID WICPixelFormat64bppRGBAHalf пикселей.</span><span class="sxs-lookup"><span data-stu-id="903a8-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="903a8-111">См. также</span><span class="sxs-lookup"><span data-stu-id="903a8-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="903a8-112">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="903a8-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="903a8-113">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="903a8-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="903a8-114">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="903a8-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="903a8-115">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="903a8-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



