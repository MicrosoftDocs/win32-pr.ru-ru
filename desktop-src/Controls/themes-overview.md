---
title: Стили оформления
description: В этом разделе приводится обзор визуальных стилей и объясняется, как настроить приложение для их использования.
ms.assetid: 9b135ccb-5e36-4657-b79c-689201047430
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bb1f8ff84f2c9f4d268ec8b50f8e7688519ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067813"
---
# <a name="visual-styles"></a><span data-ttu-id="8513a-103">Стили оформления</span><span class="sxs-lookup"><span data-stu-id="8513a-103">Visual Styles</span></span>

## <a name="purpose"></a><span data-ttu-id="8513a-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="8513a-104">Purpose</span></span>

<span data-ttu-id="8513a-105">*Визуальные стили* изменяют внешний вид общих элементов управления на основе темы, выбранной пользователем.</span><span class="sxs-lookup"><span data-stu-id="8513a-105">*Visual styles* changes the appearance of common controls based on the theme chosen by the user.</span></span> <span data-ttu-id="8513a-106">До Windows 8 необходимо специально настроить приложение для использования стилей оформления; в противном случае стандартные элементы управления приложения всегда подготавливаются к просмотру в стиле, связанном с классической темой Windows, независимо от текущей выбранной темы.</span><span class="sxs-lookup"><span data-stu-id="8513a-106">Prior to Windows 8, you must specifically configure your application to use visual styles; otherwise, the application's common controls are always rendered in the style associated with the Windows Classic theme, regardless of the currently selected theme.</span></span> <span data-ttu-id="8513a-107">В Windows 8 стили оформления не могут быть отключены, классический режим Windows больше не существует, и режим высокой контрастности был изменен для работы с визуальными стилями.</span><span class="sxs-lookup"><span data-stu-id="8513a-107">In Windows 8, visual styles can't be turned off, Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span>

<span data-ttu-id="8513a-108">В этом разделе приводится обзор визуальных стилей и объясняется, как настроить приложение для их использования.</span><span class="sxs-lookup"><span data-stu-id="8513a-108">This section provides an overview of visual styles and explains how to configure your application to use them.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8513a-109">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="8513a-109">Developer audience</span></span>

<span data-ttu-id="8513a-110">Визуальные стили предназначены для разработчиков C/C++ и конструкторов пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8513a-110">Visual styles are designed for use by C/C++ developers and UI designers.</span></span> <span data-ttu-id="8513a-111">Как правило, разработчикам нужен умеренный уровень понимания концепций программирования пользовательского интерфейса, программирования Windows API и Юникода.</span><span class="sxs-lookup"><span data-stu-id="8513a-111">In general, developers need a moderate level of understanding about UI programming concepts, Windows API programming, and Unicode.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8513a-112">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="8513a-112">Run-time requirements</span></span>

<span data-ttu-id="8513a-113">Windows Vista и более поздние операционные системы.</span><span class="sxs-lookup"><span data-stu-id="8513a-113">Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="8513a-114">Визуальные стили не поддерживаются в режиме 256-цвета.</span><span class="sxs-lookup"><span data-stu-id="8513a-114">Visual Styles are not supported in 256-color mode.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="8513a-115">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="8513a-115">In this section</span></span>

-   [<span data-ttu-id="8513a-116">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="8513a-116">What's New</span></span>](what-s-new-for-windows-8.md)
-   [<span data-ttu-id="8513a-117">Общие сведения о визуальных стилях</span><span class="sxs-lookup"><span data-stu-id="8513a-117">Visual Styles Overview</span></span>](visual-styles-overview.md)
-   [<span data-ttu-id="8513a-118">Включение стилей оформления</span><span class="sxs-lookup"><span data-stu-id="8513a-118">Enabling Visual Styles</span></span>](cookbook-overview.md)
-   [<span data-ttu-id="8513a-119">Использование стилей оформления с пользовательскими и Owner-Drawn элементами управления</span><span class="sxs-lookup"><span data-stu-id="8513a-119">Using Visual Styles with Custom and Owner-Drawn Controls</span></span>](using-visual-styles.md)
-   [<span data-ttu-id="8513a-120">Вспомогательные темы высокая контрастность</span><span class="sxs-lookup"><span data-stu-id="8513a-120">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
-   [<span data-ttu-id="8513a-121">Справочник по визуальным стилям</span><span class="sxs-lookup"><span data-stu-id="8513a-121">Visual Styles Reference</span></span>](uxctl-ref.md)

## <a name="related-topics"></a><span data-ttu-id="8513a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8513a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8513a-123">Формат файла темы</span><span class="sxs-lookup"><span data-stu-id="8513a-123">Theme File Format</span></span>](themesfileformat-overview.md)
</dt> <dt>

[<span data-ttu-id="8513a-124">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="8513a-124">Windows Controls</span></span>](window-controls.md)
</dt> </dl>

 

 




