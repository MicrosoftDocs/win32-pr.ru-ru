---
description: В этом разделе содержатся сведения о кодека собственного ДНГ, доступного через компонент Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Общие сведения о формате ДНГ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0815d6a24bb8e57e6c64b90f9e9068765838e148
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444935"
---
# <a name="dng-format-overview"></a><span data-ttu-id="ad41f-103">Общие сведения о формате ДНГ</span><span class="sxs-lookup"><span data-stu-id="ad41f-103">DNG Format Overview</span></span>

<span data-ttu-id="ad41f-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ad41f-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad41f-105">Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно приведенных здесь сведений.\]</span><span class="sxs-lookup"><span data-stu-id="ad41f-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad41f-106">В этом разделе содержатся сведения о кодека собственного ДНГ, доступного через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="ad41f-106">This topic provides information about the native DNG codec available through Windows Imaging Component (WIC).</span></span>

-   [<span data-ttu-id="ad41f-107">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="ad41f-107">Codec Identity</span></span>](#codec-identity)
-   [<span data-ttu-id="ad41f-108">Декодирование</span><span class="sxs-lookup"><span data-stu-id="ad41f-108">Decoding</span></span>](#decoding)

## <a name="codec-identity"></a><span data-ttu-id="ad41f-109">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="ad41f-109">Codec Identity</span></span>

<span data-ttu-id="ad41f-110">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="ad41f-110">The following table provides codec identification information.</span></span>



|     <span data-ttu-id="ad41f-111">Компонент</span><span class="sxs-lookup"><span data-stu-id="ad41f-111">Component</span></span>          |  <span data-ttu-id="ad41f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ad41f-112">Description</span></span>                                         |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ad41f-113">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="ad41f-113">Formal Name(s)</span></span>         | <span data-ttu-id="ad41f-114">Цифровое отрицательное (ДНГ)</span><span class="sxs-lookup"><span data-stu-id="ad41f-114">Digital Negative (DNG)</span></span>                               |
| <span data-ttu-id="ad41f-115">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="ad41f-115">File Name Extension(s)</span></span> | <span data-ttu-id="ad41f-116">DNG</span><span class="sxs-lookup"><span data-stu-id="ad41f-116">.dng</span></span>                                                 |
| <span data-ttu-id="ad41f-117">Типы MIME</span><span class="sxs-lookup"><span data-stu-id="ad41f-117">MIME type(s)</span></span>           | <span data-ttu-id="ad41f-118">Image/ДНГ</span><span class="sxs-lookup"><span data-stu-id="ad41f-118">image/DNG</span></span>                                            |
| <span data-ttu-id="ad41f-119">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="ad41f-119">Specification Support</span></span>  | <span data-ttu-id="ad41f-120">Спецификация цифровой негативной (ДНГ) версии 1.4.0.0</span><span class="sxs-lookup"><span data-stu-id="ad41f-120">Digital Negative (DNG) Specification Version 1.4.0.0</span></span> |



 

<span data-ttu-id="ad41f-121">В следующей таблице перечислены идентификаторы GUID, используемые для распознавания собственных компонентов кодека ДНГ.</span><span class="sxs-lookup"><span data-stu-id="ad41f-121">The following table lists the GUIDs used to identify the native DNG codec components.</span></span>



| <span data-ttu-id="ad41f-122">Компонент</span><span class="sxs-lookup"><span data-stu-id="ad41f-122">Component</span></span>        | <span data-ttu-id="ad41f-123">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="ad41f-123">Friendly Name</span></span>             | <span data-ttu-id="ad41f-124">Код GUID</span><span class="sxs-lookup"><span data-stu-id="ad41f-124">GUID</span></span>                                |
|------------------|---------------------------|-------------------------------------|
| <span data-ttu-id="ad41f-125">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="ad41f-125">Container Format</span></span> | <span data-ttu-id="ad41f-126">GUID \_ контаинерформатаднг</span><span class="sxs-lookup"><span data-stu-id="ad41f-126">GUID\_ContainerFormatAdng</span></span> | <span data-ttu-id="ad41f-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span><span class="sxs-lookup"><span data-stu-id="ad41f-127">f3ff6d0d-38c0-41c4-b1fe1f3824f17b84</span></span> |
| <span data-ttu-id="ad41f-128">Показан</span><span class="sxs-lookup"><span data-stu-id="ad41f-128">Decoder</span></span>          | <span data-ttu-id="ad41f-129">\_ВИКАДНГДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="ad41f-129">CLSID\_WICAdngDecoder</span></span>     | <span data-ttu-id="ad41f-130">981d9411-909e-42a7-8f5da747ff052edb</span><span class="sxs-lookup"><span data-stu-id="ad41f-130">981d9411-909e-42a7-8f5da747ff052edb</span></span> |



 

## <a name="decoding"></a><span data-ttu-id="ad41f-131">Декодирование</span><span class="sxs-lookup"><span data-stu-id="ad41f-131">Decoding</span></span>

<span data-ttu-id="ad41f-132">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="ad41f-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="ad41f-133">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="ad41f-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="ad41f-134">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="ad41f-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

<span data-ttu-id="ad41f-135">Декодер не поддерживает декодирование необработанных данных датчика и поддерживает только файлы с необработанным представлением изображений, внедренным в IFD с Невсубфилетипе, равным 1.</span><span class="sxs-lookup"><span data-stu-id="ad41f-135">The decoder does not support decoding raw sensor data and only supports files with a non-raw image representation embedded in an IFD with NewSubFileType equal to 1.</span></span>

 

 



