---
title: Новые возможности (элементы управления Windows)
description: В этом разделе описываются различия в поддержке этих стилей и визуального стиля между Windows 8 и предыдущими версиями Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488712"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="12a1c-103">Новые возможности (элементы управления Windows)</span><span class="sxs-lookup"><span data-stu-id="12a1c-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="12a1c-104">В этом разделе описываются различия в поддержке этих стилей и визуального стиля между Windows 8 и предыдущими версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="12a1c-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="12a1c-105">Через Windows 7</span><span class="sxs-lookup"><span data-stu-id="12a1c-105">Through Windows 7</span></span>

<span data-ttu-id="12a1c-106">В Windows 7 визуальные стили включены по умолчанию, но пользователь может отключить их, выбрав классическая тема Windows или отключив службу "темы".</span><span class="sxs-lookup"><span data-stu-id="12a1c-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="12a1c-107">Когда визуальные стили отключены, весь пользовательский интерфейс получает классический вид, и большинство интерфейсов API визуальных стилей недоступны.</span><span class="sxs-lookup"><span data-stu-id="12a1c-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="12a1c-108">Визуальные стили отключены в Windows 7 для поддержки различных тем высокой контрастности, а также классической темы Windows.</span><span class="sxs-lookup"><span data-stu-id="12a1c-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="12a1c-109">Если вы хотите поддерживать как визуальные стили, так и темы с высокой контрастностью в одном приложении, обычно необходимо поддерживать два отдельных пути кода для отрисовки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="12a1c-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="12a1c-110">Windows 8 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="12a1c-110">Windows 8 and Later</span></span>

<span data-ttu-id="12a1c-111">В Windows 8 стили оформления не могут быть отключены на странице **Персонализация** **параметров компьютера** или при отключении службы "темы".</span><span class="sxs-lookup"><span data-stu-id="12a1c-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="12a1c-112">Классический режим Windows больше не существует, и режим высокой контрастности был изменен для работы с визуальными стилями.</span><span class="sxs-lookup"><span data-stu-id="12a1c-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="12a1c-113">Из-за этих изменений приложения, предназначенные только для Windows 8, больше не нуждаются в двух отдельных путях кода для поддержки визуальных стилей и тем с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="12a1c-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="12a1c-114">Стили оформления в Windows 8 включают поддержку обратной совместимости в классическом режиме Windows.</span><span class="sxs-lookup"><span data-stu-id="12a1c-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="12a1c-115">Любой код отрисовки пользовательского интерфейса, работающий в предыдущих версиях, будет продолжать работать в Windows 8 без изменений.</span><span class="sxs-lookup"><span data-stu-id="12a1c-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="12a1c-116">В Windows 8, если требуется, чтобы приложение поддерживало темы с высокой контрастностью, основанные на стилях оформления, необходимо включить GUID Windows 8 в раздел совместимости манифеста приложения.</span><span class="sxs-lookup"><span data-stu-id="12a1c-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="12a1c-117">В противном случае система предполагает, что приложение предназначено для предыдущей версии и визуализирует клиентскую область, имитируя классические темы Windows с высокой контрастностью.</span><span class="sxs-lookup"><span data-stu-id="12a1c-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="12a1c-118">Дополнительные сведения см. в разделе [Поддержка тем высокая контрастность](supporting-high-contrast-themes.md).</span><span class="sxs-lookup"><span data-stu-id="12a1c-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="12a1c-119">Как и в предыдущих версиях, Windows 8 поддерживает стандартные элементы управления версии 5 и 6, а версия 5 — по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="12a1c-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="12a1c-120">Поскольку стили оформления поддерживаются только в версии 6, необходимо указать версию 6 в манифесте приложения, если необходимо применить стили оформления к общим элементам управления в клиентской области приложения.</span><span class="sxs-lookup"><span data-stu-id="12a1c-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="12a1c-121">Дополнительные сведения см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="12a1c-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12a1c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="12a1c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a1c-123">Включение стилей оформления</span><span class="sxs-lookup"><span data-stu-id="12a1c-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="12a1c-124">Вспомогательные темы высокая контрастность</span><span class="sxs-lookup"><span data-stu-id="12a1c-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="12a1c-125">Стили оформления</span><span class="sxs-lookup"><span data-stu-id="12a1c-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="12a1c-126">Общие сведения о визуальных стилях</span><span class="sxs-lookup"><span data-stu-id="12a1c-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




