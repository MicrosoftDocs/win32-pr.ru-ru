---
description: В этом разделе содержатся сведения о кодека машинного кода ICO, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Общие сведения о формате ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703039"
---
# <a name="ico-format-overview"></a><span data-ttu-id="81add-103">Общие сведения о формате ICO</span><span class="sxs-lookup"><span data-stu-id="81add-103">ICO Format Overview</span></span>

<span data-ttu-id="81add-104">В этом разделе содержатся сведения о кодека машинного кода ICO, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="81add-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="81add-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="81add-105">Codec Identity</span></span>

<span data-ttu-id="81add-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="81add-106">The following table provides codec identification information.</span></span>



|                        |                   |
|------------------------|-------------------|
| <span data-ttu-id="81add-107">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="81add-107">Formal Name(s)</span></span>         | <span data-ttu-id="81add-108">Формат значка (ICO)</span><span class="sxs-lookup"><span data-stu-id="81add-108">Icon Format (ICO)</span></span> |
| <span data-ttu-id="81add-109">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="81add-109">File Name Extension(s)</span></span> | <span data-ttu-id="81add-110">ICO</span><span class="sxs-lookup"><span data-stu-id="81add-110">ico</span></span>               |
| <span data-ttu-id="81add-111">тип MIME</span><span class="sxs-lookup"><span data-stu-id="81add-111">MIME type</span></span>              | <span data-ttu-id="81add-112">изображение или ICO</span><span class="sxs-lookup"><span data-stu-id="81add-112">image/ico</span></span>         |
| <span data-ttu-id="81add-113">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="81add-113">Specification Support</span></span>  |                   |



 

<span data-ttu-id="81add-114">В следующей таблице перечислены идентификаторы GUID, используемые для поиска компонентов кодека машинного кода ICO.</span><span class="sxs-lookup"><span data-stu-id="81add-114">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="81add-115">Компонент</span><span class="sxs-lookup"><span data-stu-id="81add-115">Component</span></span>        | <span data-ttu-id="81add-116">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="81add-116">Friendly Name</span></span>            | <span data-ttu-id="81add-117">Код GUID</span><span class="sxs-lookup"><span data-stu-id="81add-117">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="81add-118">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="81add-118">Container Format</span></span> | <span data-ttu-id="81add-119">GUID \_ контаинерформатико</span><span class="sxs-lookup"><span data-stu-id="81add-119">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="81add-120">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="81add-120">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="81add-121">Показан</span><span class="sxs-lookup"><span data-stu-id="81add-121">Decoder</span></span>          | <span data-ttu-id="81add-122">\_ВИЦИКОДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="81add-122">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="81add-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="81add-123">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="81add-124">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="81add-124">Encoder</span></span>          | <span data-ttu-id="81add-125">НЕДОСТУПНО</span><span class="sxs-lookup"><span data-stu-id="81add-125">NOT AVAILABLE</span></span>            | <span data-ttu-id="81add-126">НЕДОСТУПНО</span><span class="sxs-lookup"><span data-stu-id="81add-126">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="81add-127">Кодирование</span><span class="sxs-lookup"><span data-stu-id="81add-127">Encoding</span></span>

<span data-ttu-id="81add-128">Компонент WIC не предоставляет собственный кодировщик изображений ICO.</span><span class="sxs-lookup"><span data-stu-id="81add-128">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="81add-129">Декодирование</span><span class="sxs-lookup"><span data-stu-id="81add-129">Decoding</span></span>

<span data-ttu-id="81add-130">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="81add-130">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="81add-131">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="81add-131">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="81add-132">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="81add-132">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



