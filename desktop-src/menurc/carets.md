---
title: Крышки
description: В этом разделе рассматриваются символы крышки, которые мигающие линии, блоки или растровые изображения в клиентской области окна.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- ресурсы, символы крышки
- крышки, сведения
- Мигающие линии
- Мигающие блоки
- Мигающие растровые изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104424094"
---
# <a name="carets"></a><span data-ttu-id="918f5-108">Крышки</span><span class="sxs-lookup"><span data-stu-id="918f5-108">Carets</span></span>

<span data-ttu-id="918f5-109">*Курсор* — это мигающая линия, блок или точечный рисунок в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="918f5-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="918f5-110">Курсор обычно указывает на место, где будет вставлен текст или графика.</span><span class="sxs-lookup"><span data-stu-id="918f5-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="918f5-111">На следующем рисунке показаны некоторые распространенные вариации внешнего вида курсора.</span><span class="sxs-lookup"><span data-stu-id="918f5-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![Показывает 5 различных способов отображения курсора.](images/cscrt-01.png)

<span data-ttu-id="918f5-113">Приложения могут создавать курсоры, изменять время мерцания, а также отображать, скрывать или перемещать курсор.</span><span class="sxs-lookup"><span data-stu-id="918f5-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="918f5-114">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="918f5-114">In This Section</span></span>



| <span data-ttu-id="918f5-115">Имя</span><span class="sxs-lookup"><span data-stu-id="918f5-115">Name</span></span>                                   | <span data-ttu-id="918f5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="918f5-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="918f5-117">Около крышки</span><span class="sxs-lookup"><span data-stu-id="918f5-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="918f5-118">Описание крышки.</span><span class="sxs-lookup"><span data-stu-id="918f5-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="918f5-119">Использование крышки</span><span class="sxs-lookup"><span data-stu-id="918f5-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="918f5-120">Примеры кода, демонстрирующие выполнение задач, связанных с «крышки».</span><span class="sxs-lookup"><span data-stu-id="918f5-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="918f5-121">Ссылка на курсор</span><span class="sxs-lookup"><span data-stu-id="918f5-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="918f5-122">Содержит справочник по API.</span><span class="sxs-lookup"><span data-stu-id="918f5-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="918f5-123">Функции курсора</span><span class="sxs-lookup"><span data-stu-id="918f5-123">Caret Functions</span></span>



| <span data-ttu-id="918f5-124">Имя</span><span class="sxs-lookup"><span data-stu-id="918f5-124">Name</span></span>                                           | <span data-ttu-id="918f5-125">Описание</span><span class="sxs-lookup"><span data-stu-id="918f5-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="918f5-126">**креатекарет**</span><span class="sxs-lookup"><span data-stu-id="918f5-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="918f5-127">Создает новую фигуру для системного курсора и назначает владение курсором указанному окну.</span><span class="sxs-lookup"><span data-stu-id="918f5-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="918f5-128">Фигурой курсора может быть линия, блок или точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="918f5-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="918f5-129">**дестройкарет**</span><span class="sxs-lookup"><span data-stu-id="918f5-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="918f5-130">Уничтожает текущую фигуру курсора, освобождает курсор от окна и удаляет курсор с экрана.</span><span class="sxs-lookup"><span data-stu-id="918f5-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="918f5-131">**жеткаретблинктиме**</span><span class="sxs-lookup"><span data-stu-id="918f5-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="918f5-132">Возвращает время, необходимое для инвертирования пикселов курсора.</span><span class="sxs-lookup"><span data-stu-id="918f5-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="918f5-133">Пользователь может задать это значение.</span><span class="sxs-lookup"><span data-stu-id="918f5-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="918f5-134">**жеткаретпос**</span><span class="sxs-lookup"><span data-stu-id="918f5-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="918f5-135">Копирует позицию курсора в указанную структуру [**точек**](/previous-versions//dd162805(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="918f5-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="918f5-136">**хидекарет**</span><span class="sxs-lookup"><span data-stu-id="918f5-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="918f5-137">Удаляет курсор с экрана.</span><span class="sxs-lookup"><span data-stu-id="918f5-137">Removes the caret from the screen.</span></span> <span data-ttu-id="918f5-138">При скрытии курсора текущая фигура не уничтожается или делается недействительной точка вставки.</span><span class="sxs-lookup"><span data-stu-id="918f5-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="918f5-139">**сеткаретблинктиме**</span><span class="sxs-lookup"><span data-stu-id="918f5-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="918f5-140">Устанавливает время мигания курсора на указанное число миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="918f5-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="918f5-141">Время мерцания — это затраченное время в миллисекундах, необходимое для инвертирования пикселов курсора.</span><span class="sxs-lookup"><span data-stu-id="918f5-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="918f5-142">**сеткаретпос**</span><span class="sxs-lookup"><span data-stu-id="918f5-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="918f5-143">Перемещает курсор к указанным координатам.</span><span class="sxs-lookup"><span data-stu-id="918f5-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="918f5-144">Если окно, которому принадлежит курсор, было создано с использованием стиля класса **CS \_ овндк** , то указанные координаты будут подвергаться режиму сопоставления контекста устройства, связанного с этим окном.</span><span class="sxs-lookup"><span data-stu-id="918f5-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="918f5-145">**шовкарет**</span><span class="sxs-lookup"><span data-stu-id="918f5-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="918f5-146">Делает курсор видимым на экране в текущей позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="918f5-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="918f5-147">Когда курсор станет видимым, он начинает мигать автоматически.</span><span class="sxs-lookup"><span data-stu-id="918f5-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

