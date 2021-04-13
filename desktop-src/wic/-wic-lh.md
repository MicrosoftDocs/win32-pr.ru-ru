---
description: Компонент обработки изображений Windows
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Компонент обработки изображений Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265445"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="6675a-103">Компонент обработки изображений Windows</span><span class="sxs-lookup"><span data-stu-id="6675a-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="6675a-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="6675a-104">Purpose</span></span>

<span data-ttu-id="6675a-105">Компонент Windows Imaging Component (WIC) — это расширяемая платформа, которая предоставляет низкоуровневые API для цифровых изображений.</span><span class="sxs-lookup"><span data-stu-id="6675a-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="6675a-106">WIC поддерживает стандартные форматы веб-изображений, большие динамические изображения диапазона и данные необработанной камеры.</span><span class="sxs-lookup"><span data-stu-id="6675a-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="6675a-107">WIC также поддерживает следующие дополнительные функции:</span><span class="sxs-lookup"><span data-stu-id="6675a-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="6675a-108">Встроенная поддержка стандартных форматов метаданных</span><span class="sxs-lookup"><span data-stu-id="6675a-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="6675a-109">Расширяемая платформа для кодеков изображений, форматов пикселей и форматов метаданных.</span><span class="sxs-lookup"><span data-stu-id="6675a-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="6675a-110">Поддержка широкого диапазона поддерживаемых форматов пикселей.</span><span class="sxs-lookup"><span data-stu-id="6675a-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="6675a-111">Поддержка высокого цвета; включая 30-разрядный расширенный диапазон, 30-разрядную с высокой точностью и 48-разрядный формат пикселей с высокой точностью и шириной в один цвет.</span><span class="sxs-lookup"><span data-stu-id="6675a-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="6675a-112">Декодирование последовательного изображения.</span><span class="sxs-lookup"><span data-stu-id="6675a-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6675a-113">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="6675a-113">Developer Audience</span></span>

<span data-ttu-id="6675a-114">Компонент WIC разработан в соответствии с потребностями следующих классов разработчиков:</span><span class="sxs-lookup"><span data-stu-id="6675a-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="6675a-115">Разработчики, считывающие и записывающие данные изображений в приложении.</span><span class="sxs-lookup"><span data-stu-id="6675a-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="6675a-116">Разработчики, считывающие и записывающие метаданные изображений в приложении.</span><span class="sxs-lookup"><span data-stu-id="6675a-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="6675a-117">Разработчики, которым требуется обнаружение кодеков во время выполнения для вновь разрабатываемых или реализованных кодеков изображений.</span><span class="sxs-lookup"><span data-stu-id="6675a-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="6675a-118">Разработчики разрабатывает или реализуют новые кодеки изображений и форматы метаданных.</span><span class="sxs-lookup"><span data-stu-id="6675a-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="6675a-119">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6675a-119">In this section</span></span>



| <span data-ttu-id="6675a-120">Раздел</span><span class="sxs-lookup"><span data-stu-id="6675a-120">Topic</span></span>                                                                 | <span data-ttu-id="6675a-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6675a-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="6675a-122">Новые возможности WIC</span><span class="sxs-lookup"><span data-stu-id="6675a-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="6675a-123">Руководство по программированию</span><span class="sxs-lookup"><span data-stu-id="6675a-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="6675a-124">Описывает, как использовать API-интерфейсы WIC.</span><span class="sxs-lookup"><span data-stu-id="6675a-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="6675a-125">Ссылки</span><span class="sxs-lookup"><span data-stu-id="6675a-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="6675a-126">Содержит ссылку на API-интерфейсы WIC.</span><span class="sxs-lookup"><span data-stu-id="6675a-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="6675a-127">Примеры WIC</span><span class="sxs-lookup"><span data-stu-id="6675a-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="6675a-128">Предоставляет примеры для WIC.</span><span class="sxs-lookup"><span data-stu-id="6675a-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="6675a-129">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="6675a-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="6675a-130">Определяет термины, используемые в WIC.</span><span class="sxs-lookup"><span data-stu-id="6675a-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




