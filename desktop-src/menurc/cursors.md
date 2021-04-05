---
title: Курсоры
description: В этом разделе рассматриваются курсоры, которые представляют собой небольшие изображения, расположение которых на экране управляется указывающим устройством, например мышью, пером или трекболом.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- ресурсы, курсоры
- курсоры, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9014befcc41161d7491af97186b33088f508dd8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068055"
---
# <a name="cursors"></a><span data-ttu-id="22bc7-105">Курсоры</span><span class="sxs-lookup"><span data-stu-id="22bc7-105">Cursors</span></span>

<span data-ttu-id="22bc7-106">Курсор представляет собой небольшое изображение, положение которого на экране управляется указывающим устройством, например мышью, пером или трекболом.</span><span class="sxs-lookup"><span data-stu-id="22bc7-106">A cursor is a small picture whose location on the screen is controlled by a pointing device, such as a mouse, pen, or trackball.</span></span> <span data-ttu-id="22bc7-107">В оставшейся части этого обзора термин «мышь» относится к любому указывающему устройству.</span><span class="sxs-lookup"><span data-stu-id="22bc7-107">In the remainder of this overview, the term mouse refers to any pointing device.</span></span>

<span data-ttu-id="22bc7-108">Когда пользователь перемещает мышь, система перемещает курсор соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="22bc7-108">When the user moves the mouse, the system moves the cursor accordingly.</span></span> <span data-ttu-id="22bc7-109">Функции курсора позволяют приложениям создавать, загружать, отображать, анимировать, перемещать, ограничивать и удалять курсоры.</span><span class="sxs-lookup"><span data-stu-id="22bc7-109">The cursor functions enable applications to create, load, display, animate, move, confine, and destroy cursors.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="22bc7-110">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="22bc7-110">In This Section</span></span>



| <span data-ttu-id="22bc7-111">Имя</span><span class="sxs-lookup"><span data-stu-id="22bc7-111">Name</span></span>                                     | <span data-ttu-id="22bc7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="22bc7-112">Description</span></span>                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="22bc7-113">О курсорах</span><span class="sxs-lookup"><span data-stu-id="22bc7-113">About Cursors</span></span>](about-cursors.md)       | <span data-ttu-id="22bc7-114">Описывает стандартные курсоры.</span><span class="sxs-lookup"><span data-stu-id="22bc7-114">Discusses the standard cursors.</span></span><br/>                    |
| [<span data-ttu-id="22bc7-115">Использование курсоров</span><span class="sxs-lookup"><span data-stu-id="22bc7-115">Using Cursors</span></span>](using-cursors.md)       | <span data-ttu-id="22bc7-116">Описывает, как выполнять задачи, связанные с курсорами.</span><span class="sxs-lookup"><span data-stu-id="22bc7-116">Discusses how to perform tasks related to cursors.</span></span><br/> |
| [<span data-ttu-id="22bc7-117">Справочник по курсорам</span><span class="sxs-lookup"><span data-stu-id="22bc7-117">Cursor Reference</span></span>](cursor-reference.md) | <span data-ttu-id="22bc7-118">Содержит справочник по API.</span><span class="sxs-lookup"><span data-stu-id="22bc7-118">Contains the API reference.</span></span><br/>                        |



 

### <a name="cursor-functions"></a><span data-ttu-id="22bc7-119">Функции работы с курсорами</span><span class="sxs-lookup"><span data-stu-id="22bc7-119">Cursor Functions</span></span>



| <span data-ttu-id="22bc7-120">Имя</span><span class="sxs-lookup"><span data-stu-id="22bc7-120">Name</span></span>                                                 | <span data-ttu-id="22bc7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="22bc7-121">Description</span></span>                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22bc7-122">**клипкурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-122">**ClipCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | <span data-ttu-id="22bc7-123">Ограничивает курсор на прямоугольную область на экране.</span><span class="sxs-lookup"><span data-stu-id="22bc7-123">Confines the cursor to a rectangular area on the screen.</span></span> <span data-ttu-id="22bc7-124">Если последующая позиция курсора (заданная функцией [**сеткурсорпос**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) или мышью) находится за пределами прямоугольника, система автоматически настраивает позицию курсора внутри прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="22bc7-124">If a subsequent cursor position (set by the [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) function or the mouse) lies outside the rectangle, the system automatically adjusts the position to keep the cursor inside the rectangular area.</span></span> <br/> |
| [<span data-ttu-id="22bc7-125">**копикурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-125">**CopyCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | <span data-ttu-id="22bc7-126">Копирует указанный курсор.</span><span class="sxs-lookup"><span data-stu-id="22bc7-126">Copies the specified cursor.</span></span> <br/>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="22bc7-127">**креатекурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-127">**CreateCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | <span data-ttu-id="22bc7-128">Создает курсор с указанным размером, битовым шаблоном и активной назначением.</span><span class="sxs-lookup"><span data-stu-id="22bc7-128">Creates a cursor having the specified size, bit patterns, and hot spot.</span></span> <br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="22bc7-129">**дестройкурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-129">**DestroyCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | <span data-ttu-id="22bc7-130">Уничтожает курсор и освобождает память, занятую курсором.</span><span class="sxs-lookup"><span data-stu-id="22bc7-130">Destroys a cursor and frees any memory the cursor occupied.</span></span> <span data-ttu-id="22bc7-131">Не используйте эту функцию для уничтожения общего курсора.</span><span class="sxs-lookup"><span data-stu-id="22bc7-131">Do not use this function to destroy a shared cursor.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="22bc7-132">**жетклипкурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-132">**GetClipCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | <span data-ttu-id="22bc7-133">Получает экранные координаты прямоугольной области, до которой находится курсор.</span><span class="sxs-lookup"><span data-stu-id="22bc7-133">Retrieves the screen coordinates of the rectangular area to which the cursor is confined.</span></span> <br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="22bc7-134">**Навести курсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-134">**GetCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | <span data-ttu-id="22bc7-135">Извлекает маркер текущего курсора.</span><span class="sxs-lookup"><span data-stu-id="22bc7-135">Retrieves a handle to the current cursor.</span></span> <br/>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="22bc7-136">**жеткурсоринфо**</span><span class="sxs-lookup"><span data-stu-id="22bc7-136">**GetCursorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | <span data-ttu-id="22bc7-137">Получает сведения о глобальном курсоре.</span><span class="sxs-lookup"><span data-stu-id="22bc7-137">Retrieves information about the global cursor.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="22bc7-138">**жеткурсорпос**</span><span class="sxs-lookup"><span data-stu-id="22bc7-138">**GetCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | <span data-ttu-id="22bc7-139">Получает позицию курсора в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="22bc7-139">Retrieves the cursor's position, in screen coordinates.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="22bc7-140">**жетфисикалкурсорпос**</span><span class="sxs-lookup"><span data-stu-id="22bc7-140">**GetPhysicalCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | <span data-ttu-id="22bc7-141">Получает позицию курсора в физических координатах.</span><span class="sxs-lookup"><span data-stu-id="22bc7-141">Retrieves the position of the cursor in physical coordinates.</span></span><br/>                                                                                                                                                                                                                               |
| [<span data-ttu-id="22bc7-142">**лоадкурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-142">**LoadCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | <span data-ttu-id="22bc7-143">Загружает указанный ресурс курсора из исполняемого файла (. EXE) файл, связанный с экземпляром приложения.</span><span class="sxs-lookup"><span data-stu-id="22bc7-143">Loads the specified cursor resource from the executable (.EXE) file associated with an application instance.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="22bc7-144">**лоадкурсорфромфиле**</span><span class="sxs-lookup"><span data-stu-id="22bc7-144">**LoadCursorFromFile**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | <span data-ttu-id="22bc7-145">Создает курсор на основе данных, содержащихся в файле.</span><span class="sxs-lookup"><span data-stu-id="22bc7-145">Creates a cursor based on data contained in a file.</span></span> <br/>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="22bc7-146">**сеткурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-146">**SetCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | <span data-ttu-id="22bc7-147">Задает форму курсора.</span><span class="sxs-lookup"><span data-stu-id="22bc7-147">Sets the cursor shape.</span></span> <br/>                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="22bc7-148">**SetCursorPos**</span><span class="sxs-lookup"><span data-stu-id="22bc7-148">**SetCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | <span data-ttu-id="22bc7-149">Перемещает курсор к указанным экранным координатам.</span><span class="sxs-lookup"><span data-stu-id="22bc7-149">Moves the cursor to the specified screen coordinates.</span></span> <span data-ttu-id="22bc7-150">Если новые координаты находятся не внутри прямоугольника экрана, заданного последним вызовом функции [**клипкурсор**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) , система автоматически настраивает координаты таким образом, чтобы курсор оставался внутри прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="22bc7-150">If the new coordinates are not within the screen rectangle set by the most recent [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) function call, the system automatically adjusts the coordinates so that the cursor stays within the rectangle.</span></span> <br/>    |
| [<span data-ttu-id="22bc7-151">**сетфисикалкурсорпос**</span><span class="sxs-lookup"><span data-stu-id="22bc7-151">**SetPhysicalCursorPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | <span data-ttu-id="22bc7-152">Задает позицию курсора в физических координатах.</span><span class="sxs-lookup"><span data-stu-id="22bc7-152">Sets the position of the cursor in physical coordinates.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="22bc7-153">**сетсистемкурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-153">**SetSystemCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | <span data-ttu-id="22bc7-154">Позволяет приложению настраивать системные курсоры.</span><span class="sxs-lookup"><span data-stu-id="22bc7-154">Enables an application to customize the system cursors.</span></span> <span data-ttu-id="22bc7-155">Он заменяет содержимое системного курсора, заданное параметром *ID* , на содержимое курсора, указанного параметром *хкур* , а затем уничтожает *хкур*.</span><span class="sxs-lookup"><span data-stu-id="22bc7-155">It replaces the contents of the system cursor specified by the *id* parameter with the contents of the cursor specified by the *hcur* parameter and then destroys *hcur*.</span></span> <br/>                                                          |
| [<span data-ttu-id="22bc7-156">**шовкурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-156">**ShowCursor**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | <span data-ttu-id="22bc7-157">Отображает или скрывает курсор.</span><span class="sxs-lookup"><span data-stu-id="22bc7-157">Displays or hides the cursor.</span></span> <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a><span data-ttu-id="22bc7-158">Уведомления курсора</span><span class="sxs-lookup"><span data-stu-id="22bc7-158">Cursor Notifications</span></span>



| <span data-ttu-id="22bc7-159">Имя</span><span class="sxs-lookup"><span data-stu-id="22bc7-159">Name</span></span>                                  | <span data-ttu-id="22bc7-160">Описание</span><span class="sxs-lookup"><span data-stu-id="22bc7-160">Description</span></span>                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22bc7-161">**WM \_ сеткурсор**</span><span class="sxs-lookup"><span data-stu-id="22bc7-161">**WM\_SETCURSOR**</span></span>](wm-setcursor.md) | <span data-ttu-id="22bc7-162">Отправляется в окно, если указатель мыши вызывает перемещение курсора в пределах окна, а ввод с помощью мыши не фиксируется.</span><span class="sxs-lookup"><span data-stu-id="22bc7-162">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span> <br/> |



 

### <a name="cursor-structures"></a><span data-ttu-id="22bc7-163">Структуры курсоров</span><span class="sxs-lookup"><span data-stu-id="22bc7-163">Cursor Structures</span></span>



| <span data-ttu-id="22bc7-164">Имя</span><span class="sxs-lookup"><span data-stu-id="22bc7-164">Name</span></span>                             | <span data-ttu-id="22bc7-165">Описание</span><span class="sxs-lookup"><span data-stu-id="22bc7-165">Description</span></span>                                    |
|----------------------------------|------------------------------------------------|
| [<span data-ttu-id="22bc7-166">**курсоринфо**</span><span class="sxs-lookup"><span data-stu-id="22bc7-166">**CURSORINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-cursorinfo) | <span data-ttu-id="22bc7-167">Содержит сведения о глобальных курсорах.</span><span class="sxs-lookup"><span data-stu-id="22bc7-167">Contains global cursor information.</span></span><br/> |



 

 

 





