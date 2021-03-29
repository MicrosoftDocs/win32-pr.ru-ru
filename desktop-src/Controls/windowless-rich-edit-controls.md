---
title: Безоконное редактирование элементов управления
description: В этом разделе содержатся сведения об элементах программирования, используемых в безоконных элементах управления "поле ввода".
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067578"
---
# <a name="windowless-rich-edit-controls"></a><span data-ttu-id="83043-103">Безоконное редактирование элементов управления</span><span class="sxs-lookup"><span data-stu-id="83043-103">Windowless Rich Edit Controls</span></span>

<span data-ttu-id="83043-104">В этом разделе содержатся сведения об элементах программирования, используемых в безоконных элементах управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="83043-104">This section contains information about the programming elements used with windowless rich edit controls.</span></span> <span data-ttu-id="83043-105">Модель COM определяет набор интерфейсов для поддержки безоконных объектов.</span><span class="sxs-lookup"><span data-stu-id="83043-105">The Component Object Model (COM) defines a set of interfaces to support windowless objects.</span></span> <span data-ttu-id="83043-106">Объекты без окон могут входить в активное состояние, не имея собственного окна, а использовать окно своего контейнера.</span><span class="sxs-lookup"><span data-stu-id="83043-106">Windowless objects can enter the in-place active state without having their own window, but rather use the window of their container.</span></span> <span data-ttu-id="83043-107">Следовательно, безоконный объект использует меньше системных ресурсов и обеспечивает лучшую производительность благодаря более быстрой активации и деактивации.</span><span class="sxs-lookup"><span data-stu-id="83043-107">Consequently, a windowless object uses fewer system resources and gives better performance through faster activation and deactivation.</span></span> <span data-ttu-id="83043-108">Кроме того, объекты без окон могут быть непрямоугольными и прозрачными.</span><span class="sxs-lookup"><span data-stu-id="83043-108">In addition, windowless objects can be nonrectangular and transparent.</span></span>

### <a name="overviews"></a><span data-ttu-id="83043-109">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="83043-109">Overviews</span></span>



| <span data-ttu-id="83043-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="83043-110">Topic</span></span>                                                                          | <span data-ttu-id="83043-111">Содержимое</span><span class="sxs-lookup"><span data-stu-id="83043-111">Contents</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83043-112">О безоконном редактировании элементов управления</span><span class="sxs-lookup"><span data-stu-id="83043-112">About Windowless Rich Edit Controls</span></span>](about-windowless-rich-edit-controls.md) | <span data-ttu-id="83043-113">Безоконный элемент управления "поле ввода", также называемый объектом текстовых служб, является объектом, предоставляющим функциональные возможности [элемента управления Rich Edit](rich-edit-controls.md) без предоставления окна.</span><span class="sxs-lookup"><span data-stu-id="83043-113">A windowless rich edit control, also known as a text services object, is an object that provides the functionality of a [rich edit control](rich-edit-controls.md) without providing the window.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="83043-114">Функции</span><span class="sxs-lookup"><span data-stu-id="83043-114">Functions</span></span>



| <span data-ttu-id="83043-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="83043-115">Topic</span></span>                                            | <span data-ttu-id="83043-116">Содержимое</span><span class="sxs-lookup"><span data-stu-id="83043-116">Contents</span></span>                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83043-117">**креатетекстсервицес**</span><span class="sxs-lookup"><span data-stu-id="83043-117">**CreateTextServices**</span></span>](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | <span data-ttu-id="83043-118">Функция [**креатетекстсервицес**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) создает экземпляр объекта текстовых служб.</span><span class="sxs-lookup"><span data-stu-id="83043-118">The [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) function creates an instance of a text services object.</span></span> <span data-ttu-id="83043-119">Объект текстовых служб поддерживает различные интерфейсы, включая [**итекстсервицес**](/windows/desktop/api/Textserv/nl-textserv-itextservices) и объектную модель текста (Tom).</span><span class="sxs-lookup"><span data-stu-id="83043-119">The text services object supports a variety of interfaces, including [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) and the Text Object Model (TOM).</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="83043-120">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="83043-120">Interfaces</span></span>



| <span data-ttu-id="83043-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="83043-121">Topic</span></span>                                  | <span data-ttu-id="83043-122">Содержимое</span><span class="sxs-lookup"><span data-stu-id="83043-122">Contents</span></span>                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83043-123">**итекссост**</span><span class="sxs-lookup"><span data-stu-id="83043-123">**ITextHost**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | <span data-ttu-id="83043-124">Интерфейс [**итекссост**](/windows/desktop/api/Textserv/nl-textserv-itexthost) используется объектом текстовых служб для получения служб текстового размещения.</span><span class="sxs-lookup"><span data-stu-id="83043-124">The [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) interface is used by a text services object to obtain text host services.</span></span><br/> |
| [<span data-ttu-id="83043-125">**итекстсервицес**</span><span class="sxs-lookup"><span data-stu-id="83043-125">**ITextServices**</span></span>](/windows/desktop/api/Textserv/nl-textserv-itextservices) | <span data-ttu-id="83043-126">Расширяет том, чтобы предоставить дополнительные функциональные возможности для работы без окон.</span><span class="sxs-lookup"><span data-stu-id="83043-126">Extends the TOM to provide extra functionality for windowless operation.</span></span><br/>                                     |



 

 

 





