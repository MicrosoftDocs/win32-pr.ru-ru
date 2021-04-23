---
description: В этом разделе содержатся сведения о кодека собственного ДНГ, доступного через компонент Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Общие сведения о формате ДНГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345815"
---
# <a name="dng-format-overview"></a><span data-ttu-id="7ff77-103">Общие сведения о формате ДНГ</span><span class="sxs-lookup"><span data-stu-id="7ff77-103">DNG Format Overview</span></span>

<span data-ttu-id="7ff77-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="7ff77-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ff77-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="7ff77-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ff77-106">В этом разделе содержатся сведения о кодека собственного ДНГ, доступного через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7ff77-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="7ff77-107">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="7ff77-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="7ff77-108">Декодирование</span><span class="sxs-lookup"><span data-stu-id="7ff77-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="7ff77-109">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="7ff77-109">Codec Identity</span></span>

<span data-ttu-id="7ff77-110">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="7ff77-110">The following table provides codec identification information.</span></span>



|                        |                                                      |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="7ff77-111">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="7ff77-111">Formal Name(s)</span></span>         | <span data-ttu-id="7ff77-112">Цифровое отрицательное (ДНГ)</span><span class="sxs-lookup"><span data-stu-id="7ff77-112">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="7ff77-113">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="7ff77-113">File Name Extension(s)</span></span> | <span data-ttu-id="7ff77-114">DNG</span><span class="sxs-lookup"><span data-stu-id="7ff77-114">.dng</span></span>                                                 |
| <span data-ttu-id="7ff77-115">Типы MIME</span><span class="sxs-lookup"><span data-stu-id="7ff77-115">MIME type(s)</span></span>           | <span data-ttu-id="7ff77-116">Image/ДНГ</span><span class="sxs-lookup"><span data-stu-id="7ff77-116">image/DNG</span></span>                                            |
| <span data-ttu-id="7ff77-117">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="7ff77-117">Specification Support</span></span>  | <span data-ttu-id="7ff77-118">Спецификация цифровой негативной (ДНГ) версии 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="7ff77-118">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="7ff77-119">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека ДНГ.</span><span class="sxs-lookup"><span data-stu-id="7ff77-119">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="7ff77-120">Компонент</span><span class="sxs-lookup"><span data-stu-id="7ff77-120">Component</span></span>        | <span data-ttu-id="7ff77-121">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="7ff77-121">Friendly Name</span></span>             | <span data-ttu-id="7ff77-122">Код GUID</span><span class="sxs-lookup"><span data-stu-id="7ff77-122">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="7ff77-123">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="7ff77-123">Container Format</span></span> | <span data-ttu-id="7ff77-124">GUID \_ контаинерформатаднг</span><span class="sxs-lookup"><span data-stu-id="7ff77-124">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="7ff77-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="7ff77-125">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="7ff77-126">Показан</span><span class="sxs-lookup"><span data-stu-id="7ff77-126">Decoder</span></span>          | <span data-ttu-id="7ff77-127">\_ВИКАДНГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="7ff77-127">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="7ff77-128">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="7ff77-128">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="7ff77-129">Декодирование</span><span class="sxs-lookup"><span data-stu-id="7ff77-129">Decoding</span></span>

<span data-ttu-id="7ff77-130">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="7ff77-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="7ff77-131">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="7ff77-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="7ff77-132">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="7ff77-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="7ff77-133">Декодер не поддерживает декодирование необработанных данных датчика и поддерживает только файлы с необработанным представлением изображений, внедренным в IFD с Невсубфилетипе, равным 1.</span><span class="sxs-lookup"><span data-stu-id="7ff77-133">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



