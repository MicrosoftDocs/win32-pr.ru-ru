---
description: 'Методы Image:: Save и Image:: Савеадд класса Image получают Объект EncoderParameters, содержащий массив объектов EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Константы кодировщика изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264077"
---
# <a name="image-encoder-constants"></a><span data-ttu-id="30e20-103">Константы кодировщика изображений</span><span class="sxs-lookup"><span data-stu-id="30e20-103">Image Encoder Constants</span></span>

<span data-ttu-id="30e20-104">Методы [Image:: Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) и [Image:: савеадд](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) класса [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) получают объект [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) , содержащий массив объектов [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="30e20-104">The [Image::Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) and [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class receive an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that contains an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="30e20-105">Каждый объект **EncoderParameter** имеет элемент данных GUID, указывающий категорию параметра.</span><span class="sxs-lookup"><span data-stu-id="30e20-105">Each **EncoderParameter** object has a GUID data member that specifies the parameter category.</span></span> <span data-ttu-id="30e20-106">Следующие константы, определенные в Гдиплусимагинг. h, представляют идентификаторы GUID, указывающие различные категории параметров.</span><span class="sxs-lookup"><span data-stu-id="30e20-106">The following constants, defined in Gdiplusimaging.h, represent GUIDs that specify the various parameter categories.</span></span>

-   <span data-ttu-id="30e20-107">енкодерчроминанцетабле</span><span class="sxs-lookup"><span data-stu-id="30e20-107">EncoderChrominanceTable</span></span>
-   <span data-ttu-id="30e20-108">енкодерколордепс</span><span class="sxs-lookup"><span data-stu-id="30e20-108">EncoderColorDepth</span></span>
-   <span data-ttu-id="30e20-109">енкодерколорспаце</span><span class="sxs-lookup"><span data-stu-id="30e20-109">EncoderColorSpace</span></span>
-   <span data-ttu-id="30e20-110">енкодеркомпрессион</span><span class="sxs-lookup"><span data-stu-id="30e20-110">EncoderCompression</span></span>
-   <span data-ttu-id="30e20-111">енкодерлуминанцетабле</span><span class="sxs-lookup"><span data-stu-id="30e20-111">EncoderLuminanceTable</span></span>
-   <span data-ttu-id="30e20-112">енкодеркуалити</span><span class="sxs-lookup"><span data-stu-id="30e20-112">EncoderQuality</span></span>
-   <span data-ttu-id="30e20-113">енкодеррендермесод</span><span class="sxs-lookup"><span data-stu-id="30e20-113">EncoderRenderMethod</span></span>
-   <span data-ttu-id="30e20-114">енкодерсавефлаг</span><span class="sxs-lookup"><span data-stu-id="30e20-114">EncoderSaveFlag</span></span>
-   <span data-ttu-id="30e20-115">енкодерсканмесод</span><span class="sxs-lookup"><span data-stu-id="30e20-115">EncoderScanMethod</span></span>
-   <span data-ttu-id="30e20-116">енкодертрансформатион</span><span class="sxs-lookup"><span data-stu-id="30e20-116">EncoderTransformation</span></span>
-   <span data-ttu-id="30e20-117">EncoderVersion</span><span class="sxs-lookup"><span data-stu-id="30e20-117">EncoderVersion</span></span>
-   <span data-ttu-id="30e20-118">енкодеримажеитемс</span><span class="sxs-lookup"><span data-stu-id="30e20-118">EncoderImageItems</span></span>
-   <span data-ttu-id="30e20-119">енкодерсавеаскмик</span><span class="sxs-lookup"><span data-stu-id="30e20-119">EncoderSaveAsCMYK</span></span>

 

 
