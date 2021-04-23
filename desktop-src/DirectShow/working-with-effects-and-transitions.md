---
description: Работа с эффектами и переходами
ms.assetid: 00e97d02-ff43-4e1f-9806-abaeb9288058
title: Работа с эффектами и переходами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99029269ac86e17246fd641341b071654582bc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999696"
---
# <a name="working-with-effects-and-transitions"></a><span data-ttu-id="0fddd-103">Работа с эффектами и переходами</span><span class="sxs-lookup"><span data-stu-id="0fddd-103">Working with Effects and Transitions</span></span>

<span data-ttu-id="0fddd-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="0fddd-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0fddd-105">Эффекты изменяют один клип, запись или композицию.</span><span class="sxs-lookup"><span data-stu-id="0fddd-105">Effects modify a single clip, track, or composition.</span></span> <span data-ttu-id="0fddd-106">Переходы создают секуес из одной или компоситионсто другой.</span><span class="sxs-lookup"><span data-stu-id="0fddd-106">Transitions create seques from one track or compositionsto another.</span></span>

<span data-ttu-id="0fddd-107">[Службы редактирования DirectShow](directshow-editing-services.md) используют объекты преобразования DirectX для воспроизведения видео и видеоэффектов.</span><span class="sxs-lookup"><span data-stu-id="0fddd-107">[DirectShow Editing Services](directshow-editing-services.md) uses DirectX Transform objects for its video transitions and video effects.</span></span> <span data-ttu-id="0fddd-108">Для видеопереходов используйте любой двухмерный входной объект преобразования DirectX.</span><span class="sxs-lookup"><span data-stu-id="0fddd-108">For video transitions, use any 2-D two-input DirectX Transform object.</span></span> <span data-ttu-id="0fddd-109">Для видеоэффектов используйте любой трехмерный один входной объект преобразования DirectX.</span><span class="sxs-lookup"><span data-stu-id="0fddd-109">For video effects, use any 2-D one-input DirectX Transform object.</span></span> <span data-ttu-id="0fddd-110">Корпорация Майкрософт больше не поддерживает разработку объектов преобразования DirectX сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="0fddd-110">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="0fddd-111">Однако некоторые из них предоставляются с помощью DirectShow, а другие предоставляются в Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0fddd-111">However, several are provided with DirectShow and others are provided with Microsoft Internet Explorer.</span></span> <span data-ttu-id="0fddd-112">Дополнительные сведения о переходах, предоставляемых в Internet Explorer, см. в разделе [Справочник по визуальным фильтрам и переходам](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0fddd-112">For more information about the transitions provided with Internet Explorer, see [Visual Filters and Transitions Reference](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms532853(v=vs.85)).</span></span>

<span data-ttu-id="0fddd-113">Для звуковых эффектов можно использовать любой фильтр "звуковые эффекты DirectShow".</span><span class="sxs-lookup"><span data-stu-id="0fddd-113">For audio effects, you can use any DirectShow audio effect filter.</span></span> <span data-ttu-id="0fddd-114">DES также предоставляет [эффекты конверта тома](volume-envelope-effect.md) для настройки тома на дорожке или клипе.</span><span class="sxs-lookup"><span data-stu-id="0fddd-114">DES also provides a [Volume Envelope Effect](volume-envelope-effect.md) for setting the volume on a track or clip.</span></span> <span data-ttu-id="0fddd-115">DES не поддерживает смену звука.</span><span class="sxs-lookup"><span data-stu-id="0fddd-115">DES does not support audio transitions.</span></span>

<span data-ttu-id="0fddd-116">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="0fddd-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="0fddd-117">Добавление эффектов и объектов перехода</span><span class="sxs-lookup"><span data-stu-id="0fddd-117">Adding Effect and Transition Objects</span></span>](adding-effect-and-transition-objects.md)
-   [<span data-ttu-id="0fddd-118">Предварительный просмотр эффектов и переходов</span><span class="sxs-lookup"><span data-stu-id="0fddd-118">Previewing Effects and Transitions</span></span>](previewing-effects-and-transitions.md)
-   [<span data-ttu-id="0fddd-119">Перечисление эффектов и переходов</span><span class="sxs-lookup"><span data-stu-id="0fddd-119">Enumerating Effects and Transitions</span></span>](enumerating-effects-and-transitions.md)
-   [<span data-ttu-id="0fddd-120">Задание свойств для эффектов и переходов</span><span class="sxs-lookup"><span data-stu-id="0fddd-120">Setting Properties on Effects and Transitions</span></span>](setting-properties-on-effects-and-transitions.md)
-   [<span data-ttu-id="0fddd-121">Направление перехода</span><span class="sxs-lookup"><span data-stu-id="0fddd-121">Transition Direction</span></span>](transition-direction.md)

## <a name="related-topics"></a><span data-ttu-id="0fddd-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0fddd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fddd-123">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="0fddd-123">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
