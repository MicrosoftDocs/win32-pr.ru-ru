---
description: В этом разделе содержатся сведения о кодека машинного кода ICO, доступном через компонент Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Общие сведения о формате ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444474"
---
# <a name="ico-format-overview"></a><span data-ttu-id="12423-103">Общие сведения о формате ICO</span><span class="sxs-lookup"><span data-stu-id="12423-103">ICO Format Overview</span></span>

<span data-ttu-id="12423-104">В этом разделе содержатся сведения о кодека машинного кода ICO, доступном через компонент Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="12423-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="12423-105">Удостоверение кодека</span><span class="sxs-lookup"><span data-stu-id="12423-105">Codec Identity</span></span>

<span data-ttu-id="12423-106">В следующей таблице приведены сведения об идентификации кодека.</span><span class="sxs-lookup"><span data-stu-id="12423-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="12423-107">Компонент</span><span class="sxs-lookup"><span data-stu-id="12423-107">Component</span></span>            | <span data-ttu-id="12423-108">Описание</span><span class="sxs-lookup"><span data-stu-id="12423-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="12423-109">Формальные имена</span><span class="sxs-lookup"><span data-stu-id="12423-109">Formal Name(s)</span></span>         | <span data-ttu-id="12423-110">Формат значка (ICO)</span><span class="sxs-lookup"><span data-stu-id="12423-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="12423-111">Расширения имени файла</span><span class="sxs-lookup"><span data-stu-id="12423-111">File Name Extension(s)</span></span> | <span data-ttu-id="12423-112">ICO</span><span class="sxs-lookup"><span data-stu-id="12423-112">ico</span></span>               |
| <span data-ttu-id="12423-113">тип MIME</span><span class="sxs-lookup"><span data-stu-id="12423-113">MIME type</span></span>              | <span data-ttu-id="12423-114">изображение или ICO</span><span class="sxs-lookup"><span data-stu-id="12423-114">image/ico</span></span>         |
| <span data-ttu-id="12423-115">Поддержка спецификаций</span><span class="sxs-lookup"><span data-stu-id="12423-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="12423-116">В следующей таблице перечислены идентификаторы GUID, используемые для поиска компонентов кодека машинного кода ICO.</span><span class="sxs-lookup"><span data-stu-id="12423-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="12423-117">Компонент</span><span class="sxs-lookup"><span data-stu-id="12423-117">Component</span></span>        | <span data-ttu-id="12423-118">Понятное имя</span><span class="sxs-lookup"><span data-stu-id="12423-118">Friendly Name</span></span>            | <span data-ttu-id="12423-119">Код GUID</span><span class="sxs-lookup"><span data-stu-id="12423-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="12423-120">Формат контейнера</span><span class="sxs-lookup"><span data-stu-id="12423-120">Container Format</span></span> | <span data-ttu-id="12423-121">GUID \_ контаинерформатико</span><span class="sxs-lookup"><span data-stu-id="12423-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="12423-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="12423-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="12423-123">Показан</span><span class="sxs-lookup"><span data-stu-id="12423-123">Decoder</span></span>          | <span data-ttu-id="12423-124">\_ВИЦИКОДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="12423-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="12423-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="12423-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="12423-126">Кодировщик</span><span class="sxs-lookup"><span data-stu-id="12423-126">Encoder</span></span>          | <span data-ttu-id="12423-127">НЕДОСТУПНО</span><span class="sxs-lookup"><span data-stu-id="12423-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="12423-128">НЕДОСТУПНО</span><span class="sxs-lookup"><span data-stu-id="12423-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="12423-129">Кодирование</span><span class="sxs-lookup"><span data-stu-id="12423-129">Encoding</span></span>

<span data-ttu-id="12423-130">Компонент WIC не предоставляет собственный кодировщик изображений ICO.</span><span class="sxs-lookup"><span data-stu-id="12423-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="12423-131">Декодирование</span><span class="sxs-lookup"><span data-stu-id="12423-131">Decoding</span></span>

<span data-ttu-id="12423-132">Интерфейс API декодирования WIC разработан как независимый от кодека, а декодирование изображений для кодеков, поддерживающих WIC, по сути является одинаковым.</span><span class="sxs-lookup"><span data-stu-id="12423-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="12423-133">Дополнительные сведения о декодировании изображений см. в разделе [Общие сведения о декодировании](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="12423-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="12423-134">Дополнительные сведения об использовании декодированных данных изображения см. в разделе [Обзор источников точечных рисунков](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="12423-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



