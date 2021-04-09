---
title: API увеличения
description: API увеличения позволяет приложениям увеличивать весь экран или части экрана, а также применять цветовые эффекты.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/08/2020
ms.locfileid: "103890208"
---
# <a name="magnification-api"></a><span data-ttu-id="1c3ac-103">API увеличения</span><span class="sxs-lookup"><span data-stu-id="1c3ac-103">Magnification API</span></span>

## <a name="purpose"></a><span data-ttu-id="1c3ac-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="1c3ac-104">Purpose</span></span>

<span data-ttu-id="1c3ac-105">API увеличения позволяет приложениям увеличивать весь экран или части экрана, а также применять цветовые эффекты.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-105">The Magnification API enables applications to magnify the entire screen or portions of the screen, and to apply color effects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1c3ac-106">Где применимо</span><span class="sxs-lookup"><span data-stu-id="1c3ac-106">Where applicable</span></span>

<span data-ttu-id="1c3ac-107">С помощью API лупы разработчики могут создавать высокотехнологические приложения на основе Windows, увеличивающие экран и применяя цветовые эффекты к увеличенному содержимому экрана.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-107">By using the Magnification API, developers can create Windows-based assistive-technology applications that magnify the screen and apply color effects to the magnified screen content.</span></span> <span data-ttu-id="1c3ac-108">Для пользователей с ослабленным зрением увеличенный размер изображения и цветовые эффекты могут помочь сделать компьютер более удобным для просмотра и использования.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-108">For users with low vision, the enlarged image size and color effects can help make the computer easier to see and use.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1c3ac-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="1c3ac-109">Developer audience</span></span>

<span data-ttu-id="1c3ac-110">API увеличения разрабатывается главным образом для разработчиков на C и C++, которые понимают программирование Windows и которые знакомы с концепциями программирования графики.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-110">The Magnification API is designed primarily for C and C++ developers who understand Windows programming and who are familiar with graphics programming concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1c3ac-111">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="1c3ac-111">Run-time requirements</span></span>

<span data-ttu-id="1c3ac-112">Первоначальный выпуск API лупы поддерживается в Windows Vista и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-112">The initial release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="1c3ac-113">Во втором выпуске добавляются возможности полноэкранного увеличения, которые поддерживаются в Windows 8 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-113">A second release adds fullscreen magnification capabilities and is supported on Windows 8 and later.</span></span>

<span data-ttu-id="1c3ac-114">API поддерживается Magnification.dll.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-114">The API is supported by Magnification.dll.</span></span> <span data-ttu-id="1c3ac-115">Чтобы скомпилировать приложение, включите увеличение. h и ссылку на увеличение. lib.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-115">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="1c3ac-116">API увеличения не поддерживается в WOW64; то есть 32-разрядное приложение с экранной лупой не будет правильно работать в 64-разрядной версии Windows.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-116">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1c3ac-117">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="1c3ac-117">In this section</span></span>

| <span data-ttu-id="1c3ac-118">Раздел</span><span class="sxs-lookup"><span data-stu-id="1c3ac-118">Topic</span></span> | <span data-ttu-id="1c3ac-119">Описание</span><span class="sxs-lookup"><span data-stu-id="1c3ac-119">Description</span></span> |
|:---|:---|
| [<span data-ttu-id="1c3ac-120">Общие сведения об API увеличения</span><span class="sxs-lookup"><span data-stu-id="1c3ac-120">Magnification API Overview</span></span>](magapi-intro.md)<br/> | <span data-ttu-id="1c3ac-121">В этом разделе описывается API для увеличения масштаба и объясняется его использование в приложении.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-121">This topic describes the Magnification API and explains how to use it in an application.</span></span><br/> |
| [<span data-ttu-id="1c3ac-122">Ссылки</span><span class="sxs-lookup"><span data-stu-id="1c3ac-122">Reference</span></span>](entry-magapi-ref.md)<br/>  | <span data-ttu-id="1c3ac-123">В этом разделе содержатся справочные сведения по API лупы.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-123">This section contains reference information for the Magnification API.</span></span><br/>|
| [<span data-ttu-id="1c3ac-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="1c3ac-124">Samples</span></span>](magapi-samples-entry.md)<br/> | <span data-ttu-id="1c3ac-125">В следующем примере приложения показано, как использовать API лупы для создания полноэкранной экранной лупы, которая увеличивает весь экран, и экранную лупу, которая увеличивает и отображает часть экрана в окне.</span><span class="sxs-lookup"><span data-stu-id="1c3ac-125">The following sample application demonstrates how to use the Magnification API to create a full screen magnifier that magnifies the entire screen, and a windowed magnifier that magnifies and displays a portion of the screen in a window.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="1c3ac-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1c3ac-126">Related topics</span></span>

<span data-ttu-id="1c3ac-127">[Веб-сайт специальных возможностей Майкрософт](https://www.microsoft.com/accessibility/), [Специальные возможности в Windows 10](/windows/apps/accessibility)</span><span class="sxs-lookup"><span data-stu-id="1c3ac-127">[Microsoft Accessibility website](https://www.microsoft.com/accessibility/), [Accessibility in Windows 10](/windows/apps/accessibility)</span></span>
