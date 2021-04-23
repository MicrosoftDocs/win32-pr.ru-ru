---
title: Методы Ипапер
description: Предоставляет объекты, которые управляются главным образом собственными интерфейсами Ипапер.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- ипапер
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258957"
---
# <a name="ipaper-methods"></a><span data-ttu-id="034f9-104">Методы Ипапер</span><span class="sxs-lookup"><span data-stu-id="034f9-104">IPaper Methods</span></span>

<span data-ttu-id="034f9-105">**Стосерве** предоставляет объекты, которые управляются главным образом с помощью собственного интерфейса **ипапер** .</span><span class="sxs-lookup"><span data-stu-id="034f9-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="034f9-106">В следующей таблице перечислены методы **ипапер** из ипапер. H в каталоге с родителем \\ Inc.</span><span class="sxs-lookup"><span data-stu-id="034f9-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="034f9-107">Метод</span><span class="sxs-lookup"><span data-stu-id="034f9-107">Method</span></span>    | <span data-ttu-id="034f9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="034f9-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="034f9-109">инитпапер</span><span class="sxs-lookup"><span data-stu-id="034f9-109">InitPaper</span></span> | <span data-ttu-id="034f9-110">Инициализирует объект бумаги и создает массив рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="034f9-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="034f9-111">Блокировка</span><span class="sxs-lookup"><span data-stu-id="034f9-111">Lock</span></span>      | <span data-ttu-id="034f9-112">Обеспечивает клиентский контроль над бумагой и блокирует другие клиенты.</span><span class="sxs-lookup"><span data-stu-id="034f9-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="034f9-113">Unlock</span><span class="sxs-lookup"><span data-stu-id="034f9-113">Unlock</span></span>    | <span data-ttu-id="034f9-114">Освобождает клиентский контроль над документом.</span><span class="sxs-lookup"><span data-stu-id="034f9-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="034f9-115">Загрузить</span><span class="sxs-lookup"><span data-stu-id="034f9-115">Load</span></span>      | <span data-ttu-id="034f9-116">Загрузка бумажного содержимого из составного файла клиента и уведомление приемников.</span><span class="sxs-lookup"><span data-stu-id="034f9-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="034f9-117">Сохранить</span><span class="sxs-lookup"><span data-stu-id="034f9-117">Save</span></span>      | <span data-ttu-id="034f9-118">Сохраняет содержимое бумаги в составной файл клиента.</span><span class="sxs-lookup"><span data-stu-id="034f9-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="034f9-119">инкстарт</span><span class="sxs-lookup"><span data-stu-id="034f9-119">InkStart</span></span>  | <span data-ttu-id="034f9-120">Начинает рисовать цветовую краску на бумаге.</span><span class="sxs-lookup"><span data-stu-id="034f9-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="034f9-121">инкдрав</span><span class="sxs-lookup"><span data-stu-id="034f9-121">InkDraw</span></span>   | <span data-ttu-id="034f9-122">Помещает точки данных рукописного ввода в электронную область бумаги.</span><span class="sxs-lookup"><span data-stu-id="034f9-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="034f9-123">инкстоп</span><span class="sxs-lookup"><span data-stu-id="034f9-123">InkStop</span></span>   | <span data-ttu-id="034f9-124">Останавливает рисование рукописного ввода на бумаге.</span><span class="sxs-lookup"><span data-stu-id="034f9-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="034f9-125">Очистка</span><span class="sxs-lookup"><span data-stu-id="034f9-125">Erase</span></span>     | <span data-ttu-id="034f9-126">Очистка текущего содержимого бумаги и уведомление приемников.</span><span class="sxs-lookup"><span data-stu-id="034f9-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="034f9-127">Изменить размер</span><span class="sxs-lookup"><span data-stu-id="034f9-127">Resize</span></span>    | <span data-ttu-id="034f9-128">Изменяет размер прямоугольника рисунка бумаги и уведомляет приемники.</span><span class="sxs-lookup"><span data-stu-id="034f9-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="034f9-129">Отрисовать</span><span class="sxs-lookup"><span data-stu-id="034f9-129">Redraw</span></span>    | <span data-ttu-id="034f9-130">Перерисовывает содержимое объекта Paper и уведомляет приемники.</span><span class="sxs-lookup"><span data-stu-id="034f9-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="034f9-131">Методы, представляющие интерес для этого примера кода в составных файлах, — это [**Загрузка**](ipaper--load.md), [**Сохранение**](ipaper--save.md)и [**перерисовка**](ipaper--redraw.md).</span><span class="sxs-lookup"><span data-stu-id="034f9-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="034f9-132">[**Инкстарт**](inkstart-method.md), [**инкдрав**](inkdraw-method.md)и [**инкстоп**](cguipaper-methods.md) — это методы, используемые клиентами для создания командных чертежей для записи последовательностей рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="034f9-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="034f9-133">Клиент, как правило, реагирует на \_ сообщение WM лбуттондовн как начало последовательности рукописного ввода, вызывая **инкстарт** в содокументе.</span><span class="sxs-lookup"><span data-stu-id="034f9-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="034f9-134">Когда пользователь перемещает мышь или перо для рисования при удерживании левой кнопки, клиент будет отвечать на повторяющиеся \_ сообщения WM MOUSEMOVE с соответствующими вызовами **инкдрав**.</span><span class="sxs-lookup"><span data-stu-id="034f9-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="034f9-135">Когда пользователь отпускает левую кнопку мыши, клиент будет отвечать на \_ сообщение WM лбуттонуп с вызовом **инкстоп**, который отмечает конец последовательности рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="034f9-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="034f9-136">[**Инкстарт**](inkstart-method.md) указывает, что Начальная высота последовательности отрисовки в координатах окна клиента.</span><span class="sxs-lookup"><span data-stu-id="034f9-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="034f9-137">Он также передает цвет и ширину выбранного в данный момент пера.</span><span class="sxs-lookup"><span data-stu-id="034f9-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="034f9-138">Клиент поддерживает эти варианты выбора. Собумага просто записывает их при вызове **инкстарт** .</span><span class="sxs-lookup"><span data-stu-id="034f9-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="034f9-139">[**Инкдрав**](inkdraw-method.md) вызывается многократно, чтобы дать сомнение об успешности координат окна, представляющих движение мыши или пера.</span><span class="sxs-lookup"><span data-stu-id="034f9-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="034f9-140">[**Инкстоп**](cguipaper-methods.md) инструктирует отметку конца документа.</span><span class="sxs-lookup"><span data-stu-id="034f9-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




