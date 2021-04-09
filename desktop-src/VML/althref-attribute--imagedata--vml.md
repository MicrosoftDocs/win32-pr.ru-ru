---
title: Атрибут Алсреф (Имажедата) (VML)
description: Атрибут Алсреф (Имажедата) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070190"
---
# <a name="althref-attribute-imagedatavml"></a><span data-ttu-id="70703-103">Атрибут Алсреф (Имажедата) (VML)</span><span class="sxs-lookup"><span data-stu-id="70703-103">AltHRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="70703-104">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="70703-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="70703-105">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="70703-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="70703-106">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="70703-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="70703-107">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="70703-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="70703-108">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="70703-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="70703-109">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="70703-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="70703-110">Указывает альтернативную ссылку для изображения.</span><span class="sxs-lookup"><span data-stu-id="70703-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="70703-111">Read/write.</span><span class="sxs-lookup"><span data-stu-id="70703-111">Read/write.</span></span> <span data-ttu-id="70703-112">**Строка**.</span><span class="sxs-lookup"><span data-stu-id="70703-112">**String**.</span></span>

<span data-ttu-id="70703-113">**Применимо к**:</span><span class="sxs-lookup"><span data-stu-id="70703-113">**Applies To**</span></span>

[<span data-ttu-id="70703-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="70703-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="70703-115">**Синтаксис тега**</span><span class="sxs-lookup"><span data-stu-id="70703-115">**Tag Syntax**</span></span>

<span data-ttu-id="70703-116"><v: *element* о:алсреф = " *выражение* " ></span><span class="sxs-lookup"><span data-stu-id="70703-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="70703-117">**Синтаксис сценария**</span><span class="sxs-lookup"><span data-stu-id="70703-117">**Script Syntax**</span></span>

<span data-ttu-id="70703-118">*element* . алсреф = "*выражение*"</span><span class="sxs-lookup"><span data-stu-id="70703-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="70703-119">*выражение* = *element*. алсреф</span><span class="sxs-lookup"><span data-stu-id="70703-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="70703-120">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="70703-120">**Remarks**</span></span>

<span data-ttu-id="70703-121">Поддерживает сохранение данных PICT через HTML переносе.</span><span class="sxs-lookup"><span data-stu-id="70703-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="70703-122">При записи в формате HTML альтернативное представление (то есть исходные данные PICT, если файл был создан из Macintosh) сохраняется.</span><span class="sxs-lookup"><span data-stu-id="70703-122">On HTML write, the alternate representation (that is, the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="70703-123">При чтении HTML **алсреф** имеет приоритет над **src**.</span><span class="sxs-lookup"><span data-stu-id="70703-123">On an HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="70703-124">*Атрибут расширений Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="70703-124">*Microsoft Office Extensions Attribute*</span></span>

 

 