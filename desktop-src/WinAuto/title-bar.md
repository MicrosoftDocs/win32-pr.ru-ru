---
title: Заголовок окна (Справочник по элементу пользовательского интерфейса MSAA)
description: В строке заголовка в верхней части окна отображается значок и строка текста, определенные в приложении.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412429"
---
# <a name="title-bar-msaa-ui-element-reference"></a><span data-ttu-id="654a4-103">Заголовок окна (Справочник по элементу пользовательского интерфейса MSAA)</span><span class="sxs-lookup"><span data-stu-id="654a4-103">Title Bar (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="654a4-104">В этом разделе описываются объекты **заголовков** для целей справочника по элементам ПОЛЬЗОВАТЕЛЬСКОГО интерфейса MSAA.</span><span class="sxs-lookup"><span data-stu-id="654a4-104">This topic describes **Title Bar** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="654a4-105">Создание объектов **заголовка** в различных ПЛАТФОРМАХ пользовательского интерфейса не описывается здесь.</span><span class="sxs-lookup"><span data-stu-id="654a4-105">How to create **Title Bar** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="654a4-106">См. справочную документацию по API для платформы пользовательского интерфейса, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="654a4-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="654a4-107">В строке заголовка в верхней части окна отображается значок и строка текста, определенные в приложении.</span><span class="sxs-lookup"><span data-stu-id="654a4-107">The title bar at the top of a window displays an application-defined icon and line of text.</span></span> <span data-ttu-id="654a4-108">Текст указывает имя приложения и указывает назначение окна.</span><span class="sxs-lookup"><span data-stu-id="654a4-108">The text specifies the name of the application and indicates the purpose of the window.</span></span> <span data-ttu-id="654a4-109">Кроме того, строка заголовка позволяет пользователю перемещать окно с помощью мыши или другого указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="654a4-109">The title bar also makes it possible for the user to move the window using a mouse or other pointing device.</span></span>

<span data-ttu-id="654a4-110">Строки заголовка содержат по крайней мере три небольшие кнопки, которые сворачиваются, развернут или восстановлены, и закрывают окно, связанное с заголовком.</span><span class="sxs-lookup"><span data-stu-id="654a4-110">Title bars contain at least three small buttons that minimize, maximize or restore, and close the window associated with the title bar.</span></span> <span data-ttu-id="654a4-111">Строки заголовка также содержат контекстно-зависимую кнопку справки.</span><span class="sxs-lookup"><span data-stu-id="654a4-111">Title bars also contain a context-sensitive Help button.</span></span> <span data-ttu-id="654a4-112">Приложения, работающие в Far-East версии операционной системы Windows, также могут содержать кнопки редактора методов ввода (IME).</span><span class="sxs-lookup"><span data-stu-id="654a4-112">Applications running in the Far-East version of the Windows operating system may also contain Input Method Editor (IME) buttons.</span></span> <span data-ttu-id="654a4-113">Microsoft Active Accessibility предоставляет эти кнопки как дочерние элементы заголовка окна.</span><span class="sxs-lookup"><span data-stu-id="654a4-113">Microsoft Active Accessibility exposes these buttons as child elements of the title bar.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="654a4-114">Методы IAccessible</span><span class="sxs-lookup"><span data-stu-id="654a4-114">IAccessible Methods</span></span>

<span data-ttu-id="654a4-115">Строки заголовка поддерживают следующие методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="654a4-115">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="654a4-116">**акчиттест**</span><span class="sxs-lookup"><span data-stu-id="654a4-116">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="654a4-117">**акклокатион**</span><span class="sxs-lookup"><span data-stu-id="654a4-117">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="654a4-118">**аккнавигате**</span><span class="sxs-lookup"><span data-stu-id="654a4-118">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="654a4-119">**аккселект**</span><span class="sxs-lookup"><span data-stu-id="654a4-119">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="654a4-120">Свойства IAccessible</span><span class="sxs-lookup"><span data-stu-id="654a4-120">IAccessible Properties</span></span>

<span data-ttu-id="654a4-121">Заголовки окон поддерживают следующие свойства [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="654a4-121">Title bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="654a4-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="654a4-122">Property</span></span></th>
<th><span data-ttu-id="654a4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="654a4-123">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="654a4-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="654a4-124"><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></span></span></td>
<td><span data-ttu-id="654a4-125">Свойство <strong>ChildCount</strong> имеет значение 5.</span><span class="sxs-lookup"><span data-stu-id="654a4-125">The <strong>ChildCount</strong> property is five.</span></span> <span data-ttu-id="654a4-126">Свойство <strong>ChildCount</strong> содержит редакторы IME и контекстно-зависимые кнопки справки, даже если они не отображаются.</span><span class="sxs-lookup"><span data-stu-id="654a4-126">The <strong>ChildCount</strong> property includes the IME and context-sensitive Help buttons even when they are not displayed.</span></span> <span data-ttu-id="654a4-127">Кнопки, которые не отображаются, имеют <strong></strong> свойство State <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="654a4-127">Buttons that are not displayed have the <strong>State</strong> property <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="654a4-128"><strong>get_accDescription</strong></span><span class="sxs-lookup"><span data-stu-id="654a4-128"><strong>get_accDescription</strong></span></span></td>
<td><span data-ttu-id="654a4-129">Свойство <strong>Description</strong> в строке заголовка: &quot; отображает имя окна и содержит элементы управления для его управления. &quot; Дочерние кнопки в заголовке окна имеют следующие описания:</span><span class="sxs-lookup"><span data-stu-id="654a4-129">The <strong>Description</strong> property of the title bar itself is: &quot;Displays the name of the window and contains controls to manipulate it.&quot; The child buttons in the title bar have the following descriptions:</span></span><br/>
<ul>
<li><span data-ttu-id="654a4-130">&quot;Перемещает окно из</span><span class="sxs-lookup"><span data-stu-id="654a4-130">&quot;Moves the window out of</span></span></li>
<li><span data-ttu-id="654a4-131">&quot;Делает окно заполненным</span><span class="sxs-lookup"><span data-stu-id="654a4-131">&quot;Makes the window full</span></span></li>
<li><span data-ttu-id="654a4-132">&quot;Помещает в окно сворачивания или</span><span class="sxs-lookup"><span data-stu-id="654a4-132">&quot;Puts a minimized or</span></span></li>
<li><span data-ttu-id="654a4-133">&quot;Закрытие окна&quot;</span><span class="sxs-lookup"><span data-stu-id="654a4-133">&quot;Closes the window&quot;</span></span></li>
<li><span data-ttu-id="654a4-134">&quot;Вводит или оставляет контекст-</span><span class="sxs-lookup"><span data-stu-id="654a4-134">&quot;Enters or leaves context-</span></span></li>
<li><span data-ttu-id="654a4-135">&quot;Открывает клавиатуру при нажатии&quot;</span><span class="sxs-lookup"><span data-stu-id="654a4-135">&quot;Brings up the keyboard when pressed&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="654a4-136"><strong>get_accName</strong></span><span class="sxs-lookup"><span data-stu-id="654a4-136"><strong>get_accName</strong></span></span></td>
<td><span data-ttu-id="654a4-137">Сама строка заголовка не поддерживает свойство <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="654a4-137">The title bar itself does not support the <strong>Name</strong> property.</span></span> <span data-ttu-id="654a4-138">Дочерние кнопки в заголовке окна имеют следующие имена:</span><span class="sxs-lookup"><span data-stu-id="654a4-138">The child buttons in the title bar have the following names:</span></span>
<ul>
<li><span data-ttu-id="654a4-139">&quot;Свернуть&quot;</span><span class="sxs-lookup"><span data-stu-id="654a4-139">&quot;Minimize&quot;</span></span></li>
<li><span data-ttu-id="654a4-140">&quot;Развернуть &quot; или &quot; восстановить &quot; ,</span><span class="sxs-lookup"><span data-stu-id="654a4-140">&quot;Maximize&quot; or &quot;Restore&quot;,</span></span></li>
<li><span data-ttu-id="654a4-141">&quot;Закрыть&quot;</span><span class="sxs-lookup"><span data-stu-id="654a4-141">&quot;Close&quot;</span></span></li>
<li><span data-ttu-id="654a4-142">&quot;Контекстная Справка&quot;</span><span class="sxs-lookup"><span data-stu-id="654a4-142">&quot;Context help&quot;</span></span></li>
<li><span data-ttu-id="654a4-143">&quot;IME&quot;</span><span class="sxs-lookup"><span data-stu-id="654a4-143">&quot;IME&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="654a4-144"><strong>get_accParent</strong></span><span class="sxs-lookup"><span data-stu-id="654a4-144"><strong>get_accParent</strong></span></span></td>
<td><span data-ttu-id="654a4-145">Свойство <strong>Parent</strong> заголовка окна является основным окном приложения ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ), которое имеет то же имя класса окон, что и заголовок окна приложения.</span><span class="sxs-lookup"><span data-stu-id="654a4-145">The <strong>Parent</strong> property of the title bar is the main application window ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) that has the same application-defined window class name as the title bar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="654a4-146"><strong>get_accRole</strong></span><span class="sxs-lookup"><span data-stu-id="654a4-146"><strong>get_accRole</strong></span></span></td>
<td><span data-ttu-id="654a4-147">Свойство <strong>Role</strong> имеет значение <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="654a4-147">The <strong>Role</strong> property is <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>.</span></span> <span data-ttu-id="654a4-148">Дочерние кнопки в строке заголовка имеют свойство <strong>Role</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="654a4-148">The child buttons in the title bar have the <strong>Role</strong> property <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="654a4-149"><strong>get_accState</strong></span><span class="sxs-lookup"><span data-stu-id="654a4-149"><strong>get_accState</strong></span></span></td>
<td><span data-ttu-id="654a4-150">Свойство <strong>State</strong> для заголовка окна и дочерних кнопок может быть сочетанием одного или нескольких из следующих <a href="object-state-constants.md">значений</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="654a4-150">The <strong>State</strong> property for the title bar and the child buttons can be a combination of one or more of the following <a href="object-state-constants.md">values</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="654a4-151"><strong>get_accValue</strong></span><span class="sxs-lookup"><span data-stu-id="654a4-151"><strong>get_accValue</strong></span></span></td>
<td><span data-ttu-id="654a4-152">Свойство <strong>value</strong> — это строка, которая совпадает с текстом, отображаемым в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="654a4-152">The <strong>Value</strong> property is a string that is the same as the text displayed in the title bar.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a><span data-ttu-id="654a4-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="654a4-153">Notes</span></span>

-   <span data-ttu-id="654a4-154">Несмотря на то, что заголовок приложения имеет свойство **State** , которое имеет [**\_ \_ фокус системы состояния**](object-state-constants.md), оно никогда не имеет **отметок состояния** [**\_ системы \_**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="654a4-154">Although an application's title bar has the **State** property flag [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md), it never has the **State** flag [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md).</span></span> <span data-ttu-id="654a4-155">Установка фокуса на заголовке окна приложения помещается в главное окно.</span><span class="sxs-lookup"><span data-stu-id="654a4-155">Setting focus to a title bar object focuses the application window.</span></span>
-   <span data-ttu-id="654a4-156">Поскольку объект заголовка окна не поддерживает [**Get \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), кнопки в заголовке окна являются простыми элементами.</span><span class="sxs-lookup"><span data-stu-id="654a4-156">Because the title bar object does not support [**get\_accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), the buttons on the title bar are simple elements.</span></span> <span data-ttu-id="654a4-157">Они не поддерживают интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) сами по себе.</span><span class="sxs-lookup"><span data-stu-id="654a4-157">They do not support the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface themselves.</span></span> <span data-ttu-id="654a4-158">Объект заголовка окна содержит сведения об этих дочерних кнопках.</span><span class="sxs-lookup"><span data-stu-id="654a4-158">The title bar object provides information about these child buttons.</span></span>
-   <span data-ttu-id="654a4-159">Поскольку строки заголовка не получают фокус и не имеют действия по умолчанию, методы [**аккдодефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) и [**Get \_ аккдефаултактион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) не поддерживаются для этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="654a4-159">Because title bars do not get focus and have no default action, the [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) and [**get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) methods are not supported for this control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="654a4-160">См. также</span><span class="sxs-lookup"><span data-stu-id="654a4-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="654a4-161">Интерфейс IAccessible</span><span class="sxs-lookup"><span data-stu-id="654a4-161">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





