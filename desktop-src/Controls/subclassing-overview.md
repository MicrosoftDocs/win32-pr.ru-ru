---
title: Подклассировать элементы управления
description: Если элемент управления выполняет практически все необходимые действия, но вам нужны еще несколько функций, можно изменить или добавить компоненты в исходный элемент управления, добавив в него подкласс.
ms.assetid: 7f558674-c8b2-4461-96ba-e139416b7a1c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c013ee317ddeee6ff80dc4a26982d40d7117950
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070720"
---
# <a name="subclassing-controls"></a><span data-ttu-id="68a58-103">Подклассировать элементы управления</span><span class="sxs-lookup"><span data-stu-id="68a58-103">Subclassing Controls</span></span>

<span data-ttu-id="68a58-104">Если элемент управления выполняет практически все необходимые действия, но вам нужны еще несколько функций, можно изменить или добавить компоненты в исходный элемент управления, добавив в него подкласс.</span><span class="sxs-lookup"><span data-stu-id="68a58-104">If a control does almost everything you want, but you need a few more features, you can change or add features to the original control by subclassing it.</span></span> <span data-ttu-id="68a58-105">Подкласс может иметь все функции существующего класса, а также любые дополнительные функции, которые вы хотите предоставить.</span><span class="sxs-lookup"><span data-stu-id="68a58-105">A subclass can have all the features of an existing class as well as any additional features you want to give it.</span></span>

<span data-ttu-id="68a58-106">В этом документе рассматривается создание подклассов и включает в себя следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="68a58-106">This document discusses how subclasses are created and includes the following topics.</span></span>

-   [<span data-ttu-id="68a58-107">Подклассировать элементы управления до ComCtl32.dll версии 6</span><span class="sxs-lookup"><span data-stu-id="68a58-107">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>](#subclassing-controls-prior-to-comctl32dll-version-6)
    -   [<span data-ttu-id="68a58-108">Хранение пользовательских данных</span><span class="sxs-lookup"><span data-stu-id="68a58-108">Storing User Data</span></span>](#storing-user-data)
    -   [<span data-ttu-id="68a58-109">Недостатки старого подхода к подклассам</span><span class="sxs-lookup"><span data-stu-id="68a58-109">Disadvantages of the Old Subclassing Approach</span></span>](#disadvantages-of-the-old-subclassing-approach)
-   [<span data-ttu-id="68a58-110">Подклассировать элементы управления с помощью ComCtl32.dll версии 6</span><span class="sxs-lookup"><span data-stu-id="68a58-110">Subclassing Controls Using ComCtl32.dll version 6</span></span>](#subclassing-controls-using-comctl32dll-version-6)
    -   [<span data-ttu-id="68a58-111">сетвиндовсубкласс</span><span class="sxs-lookup"><span data-stu-id="68a58-111">SetWindowSubclass</span></span>](#setwindowsubclass)
    -   [<span data-ttu-id="68a58-112">жетвиндовсубкласс</span><span class="sxs-lookup"><span data-stu-id="68a58-112">GetWindowSubclass</span></span>](#getwindowsubclass)
    -   [<span data-ttu-id="68a58-113">ремовевиндовсубкласс</span><span class="sxs-lookup"><span data-stu-id="68a58-113">RemoveWindowSubclass</span></span>](#removewindowsubclass)
    -   [<span data-ttu-id="68a58-114">дефсубкласспрок</span><span class="sxs-lookup"><span data-stu-id="68a58-114">DefSubclassProc</span></span>](#defsubclassproc)

## <a name="subclassing-controls-prior-to-comctl32dll-version-6"></a><span data-ttu-id="68a58-115">Подклассировать элементы управления до ComCtl32.dll версии 6</span><span class="sxs-lookup"><span data-stu-id="68a58-115">Subclassing Controls Prior to ComCtl32.dll version 6</span></span>

<span data-ttu-id="68a58-116">Можно разместить элемент управления в подклассе и сохранить данные пользователя в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="68a58-116">You can put a control in a subclass and store user data within a control.</span></span> <span data-ttu-id="68a58-117">Это делается при использовании версий ComCtl32.dll до версии 6.</span><span class="sxs-lookup"><span data-stu-id="68a58-117">You do this when you use versions of ComCtl32.dll prior to version 6.</span></span> <span data-ttu-id="68a58-118">Существуют некоторые недостатки создания подклассов с более ранними версиями ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="68a58-118">There are some disadvantages in creating subclasses with earlier versions of ComCtl32.dll.</span></span>

<span data-ttu-id="68a58-119">Чтобы создать новый элемент управления, лучше всего начать с одного из стандартных элементов управления Windows и расширить его в соответствии с конкретной потребностью.</span><span class="sxs-lookup"><span data-stu-id="68a58-119">To make a new control, it is best to start with one of the Windows common controls and extend it to fit a particular need.</span></span> <span data-ttu-id="68a58-120">Чтобы расширить элемент управления, создайте элемент управления и замените его существующую процедуру окна новой.</span><span class="sxs-lookup"><span data-stu-id="68a58-120">To extend a control, create a control and replace its existing window procedure with a new one.</span></span> <span data-ttu-id="68a58-121">Новая процедура перехватывает сообщения элемента управления и либо обрабатывает их, либо передает их в исходную процедуру для обработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68a58-121">The new procedure intercepts the control's messages and either acts on them or passes them to the original procedure for default processing.</span></span> <span data-ttu-id="68a58-122">Используйте функцию [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) или [**сетвиндовлонгптр**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) , чтобы заменить WndProc элемента управления.</span><span class="sxs-lookup"><span data-stu-id="68a58-122">Use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) or [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function to replace the WNDPROC of the control.</span></span> <span data-ttu-id="68a58-123">В следующем примере кода показано, как заменить WNDPROC.</span><span class="sxs-lookup"><span data-stu-id="68a58-123">The following code sample shows how to replace a WNDPROC.</span></span>


```
OldWndProc = (WNDPROC)SetWindowLongPtr (hButton,
GWLP_WNDPROC, (LONG_PTR)NewWndProc);
```



### <a name="storing-user-data"></a><span data-ttu-id="68a58-124">Хранение пользовательских данных</span><span class="sxs-lookup"><span data-stu-id="68a58-124">Storing User Data</span></span>

<span data-ttu-id="68a58-125">Может потребоваться сохранить данные пользователя в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="68a58-125">You might want to store user data with an individual window.</span></span> <span data-ttu-id="68a58-126">Эти данные могут использоваться новой процедурой окна для определения способа рисования элемента управления или места отправки определенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="68a58-126">This data can be used by the new window procedure to determine how to draw the control or where to send certain messages.</span></span> <span data-ttu-id="68a58-127">Например, вы можете использовать данные для хранения указателя на класс C++ в классе, который представляет элемент управления.</span><span class="sxs-lookup"><span data-stu-id="68a58-127">For example, you might use data to store a C++ class pointer to the class that represents the control.</span></span> <span data-ttu-id="68a58-128">В следующем примере кода показано, как использовать [**сбой setprop**](/windows/desktop/api/winuser/nf-winuser-setpropa) для хранения данных в окне.</span><span class="sxs-lookup"><span data-stu-id="68a58-128">The following code sample shows how to use [**SetProp**](/windows/desktop/api/winuser/nf-winuser-setpropa) to store data with a window.</span></span>


```
SetProp (hwnd, TEXT("MyData"), (HANDLE)pMyData);
```



### <a name="disadvantages-of-the-old-subclassing-approach"></a><span data-ttu-id="68a58-129">Недостатки старого подхода к подклассам</span><span class="sxs-lookup"><span data-stu-id="68a58-129">Disadvantages of the Old Subclassing Approach</span></span>

<span data-ttu-id="68a58-130">В следующем списке рассматриваются некоторые недостатки использования описанного выше подхода для подкласса элемента управления.</span><span class="sxs-lookup"><span data-stu-id="68a58-130">The following list points out some of the disadvantages of using the previously described approach to subclassing a control.</span></span>

-   <span data-ttu-id="68a58-131">Процедуру окна можно заменить только один раз.</span><span class="sxs-lookup"><span data-stu-id="68a58-131">The window procedure can only be replaced once.</span></span>
-   <span data-ttu-id="68a58-132">Удалить подкласс после его создания сложно.</span><span class="sxs-lookup"><span data-stu-id="68a58-132">It is difficult to remove a subclass after it is created.</span></span>
-   <span data-ttu-id="68a58-133">Связывание закрытых данных с окном неэффективно.</span><span class="sxs-lookup"><span data-stu-id="68a58-133">Associating private data with a window is inefficient.</span></span>
-   <span data-ttu-id="68a58-134">Чтобы вызвать следующую процедуру в цепочке подклассов, невозможно привести старую процедуру окна и вызвать ее, необходимо вызвать ее с помощью функции [**каллвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="68a58-134">To call the next procedure in a subclass chain, you cannot cast the old window procedure and call it, you must call it by using the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function.</span></span>

## <a name="subclassing-controls-using-comctl32dll-version-6"></a><span data-ttu-id="68a58-135">Подклассировать элементы управления с помощью ComCtl32.dll версии 6</span><span class="sxs-lookup"><span data-stu-id="68a58-135">Subclassing Controls Using ComCtl32.dll version 6</span></span>

> [!Note]  
> <span data-ttu-id="68a58-136">ComCtl32.dll версии 6 — только Юникод.</span><span class="sxs-lookup"><span data-stu-id="68a58-136">ComCtl32.dll version 6 is Unicode only.</span></span> <span data-ttu-id="68a58-137">Стандартные элементы управления, поддерживаемые ComCtl32.dll версии 6, не должны быть переклассами (или классами) с помощью оконных процедур ANSI.</span><span class="sxs-lookup"><span data-stu-id="68a58-137">The common controls supported by ComCtl32.dll version 6 should not be subclassed (or superclassed) with ANSI window procedures.</span></span>

 

<span data-ttu-id="68a58-138">ComCtl32.dll версии 6 содержит четыре функции, которые упрощают создание подклассов и устраняют ранее обсуждаемые недостатки.</span><span class="sxs-lookup"><span data-stu-id="68a58-138">ComCtl32.dll version 6 contains four functions that make creating subclasses easier and eliminate the disadvantages previously discussed.</span></span> <span data-ttu-id="68a58-139">Новые функции инкапсулируют управление, вовлеченное в множество наборов справочных данных, поэтому разработчик может сосредоточиться на функциях программирования, а не на управлении подклассами.</span><span class="sxs-lookup"><span data-stu-id="68a58-139">The new functions encapsulate the management involved with multiple sets of reference data, therefore the developer can focus on programming features and not on managing subclasses.</span></span> <span data-ttu-id="68a58-140">Функции подкласса:</span><span class="sxs-lookup"><span data-stu-id="68a58-140">The subclassing functions are:</span></span>

-   [<span data-ttu-id="68a58-141">**сетвиндовсубкласс**</span><span class="sxs-lookup"><span data-stu-id="68a58-141">**SetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass)
-   [<span data-ttu-id="68a58-142">**жетвиндовсубкласс**</span><span class="sxs-lookup"><span data-stu-id="68a58-142">**GetWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass)
-   [<span data-ttu-id="68a58-143">**ремовевиндовсубкласс**</span><span class="sxs-lookup"><span data-stu-id="68a58-143">**RemoveWindowSubclass**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass)
-   [<span data-ttu-id="68a58-144">**дефсубкласспрок**</span><span class="sxs-lookup"><span data-stu-id="68a58-144">**DefSubclassProc**</span></span>](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc)

### <a name="setwindowsubclass"></a><span data-ttu-id="68a58-145">сетвиндовсубкласс</span><span class="sxs-lookup"><span data-stu-id="68a58-145">SetWindowSubclass</span></span>

<span data-ttu-id="68a58-146">Эта функция используется для первоначального подкласса окна.</span><span class="sxs-lookup"><span data-stu-id="68a58-146">This function is used to initially subclass a window.</span></span> <span data-ttu-id="68a58-147">Каждый подкласс однозначно идентифицируется по адресу *пфнсубкласс* и его *уидсубкласс*.</span><span class="sxs-lookup"><span data-stu-id="68a58-147">Each subclass is uniquely identified by the address of the *pfnSubclass* and its *uIdSubclass*.</span></span> <span data-ttu-id="68a58-148">Оба параметра являются параметрами функции [**сетвиндовсубкласс**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) .</span><span class="sxs-lookup"><span data-stu-id="68a58-148">Both of these are parameters of the [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) function.</span></span> <span data-ttu-id="68a58-149">Несколько подклассов могут совместно использовать одну и ту же процедуру подкласса, и идентификатор может опознать каждый вызов.</span><span class="sxs-lookup"><span data-stu-id="68a58-149">Several subclasses can share the same subclass procedure and the ID can identify each call.</span></span> <span data-ttu-id="68a58-150">Чтобы изменить ссылочные данные, можно выполнить последующие вызовы **сетвиндовсубкласс**.</span><span class="sxs-lookup"><span data-stu-id="68a58-150">To change reference data you can make subsequent calls to **SetWindowSubclass**.</span></span> <span data-ttu-id="68a58-151">Важным преимуществом является то, что каждый экземпляр подкласса имеет собственные справочные данные.</span><span class="sxs-lookup"><span data-stu-id="68a58-151">The important advantage is that each subclass instance has its own reference data.</span></span>

<span data-ttu-id="68a58-152">Объявление процедуры-подкласса немного отличается от обычной процедуры окна, поскольку содержит два дополнительных фрагмента данных: Идентификатор подкласса и ссылочные данные.</span><span class="sxs-lookup"><span data-stu-id="68a58-152">The declaration of a subclass procedure is slightly different from a regular window procedure because it has two additional pieces of data: the subclass ID and the reference data.</span></span> <span data-ttu-id="68a58-153">Это показано в двух последних параметрах приведенного ниже объявления функции.</span><span class="sxs-lookup"><span data-stu-id="68a58-153">The last two parameters of the following function declaration show this.</span></span>


```
LRESULT CALLBACK MyWndProc (HWND hWnd, UINT msg,
WPARAM wParam, LPARAM lParam, UINT_PTR uIdSubclass,
DWORD_PTR dwRefData);
```



<span data-ttu-id="68a58-154">При каждом получении сообщения с помощью новой процедуры окна включаются идентификатор подкласса и ссылочные данные.</span><span class="sxs-lookup"><span data-stu-id="68a58-154">Every time a message is received by the new window procedure, a subclass ID and reference data are included.</span></span>

> [!Note]  
> <span data-ttu-id="68a58-155">Все строки, передаваемые в процедуру, являются строками в Юникоде, даже если в качестве определения препроцессора не указан Юникод.</span><span class="sxs-lookup"><span data-stu-id="68a58-155">All strings passed to the procedure are Unicode strings even if Unicode is not specified as a preprocessor definition.</span></span>

 

<span data-ttu-id="68a58-156">В следующем примере показана скелетная реализация процедуры окна для элемента управления с подклассом.</span><span class="sxs-lookup"><span data-stu-id="68a58-156">The following example shows a skeleton implementation of a window procedure for a subclassed control.</span></span>


```
LRESULT CALLBACK OwnerDrawButtonProc(HWND hWnd, UINT uMsg, WPARAM wParam,
                               LPARAM lParam, UINT_PTR uIdSubclass, DWORD_PTR dwRefData)
{
    switch (uMsg)
    {
    case WM_PAINT:
        .
        .
        .
        return TRUE;
    // Other cases...
    } 
    return DefSubclassProc(hWnd, uMsg, wParam, lParam);
}
```



<span data-ttu-id="68a58-157">Процедура окна может быть присоединена к элементу управления в обработчике [**WM \_ инитдиалог**](/windows/desktop/dlgbox/wm-initdialog) процедуры диалогового окна, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="68a58-157">The window procedure can be attached to the control in the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) handler of the dialog procedure, as shown in the following example.</span></span>


```
case WM_INITDIALOG:
{
    HWND button = GetDlgItem(hDlg, IDC_OWNERDRAWBUTTON);
    SetWindowSubclass(button, OwnerDrawButtonProc, 0, 0);
    return TRUE;
}
```



### <a name="getwindowsubclass"></a><span data-ttu-id="68a58-158">жетвиндовсубкласс</span><span class="sxs-lookup"><span data-stu-id="68a58-158">GetWindowSubclass</span></span>

<span data-ttu-id="68a58-159">Эта функция получает сведения о подклассе.</span><span class="sxs-lookup"><span data-stu-id="68a58-159">This function retrieves information about a subclass.</span></span> <span data-ttu-id="68a58-160">Например, можно использовать [**жетвиндовсубкласс**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) для доступа к эталонным данным.</span><span class="sxs-lookup"><span data-stu-id="68a58-160">For example, you can use [**GetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-getwindowsubclass) to access the reference data.</span></span>

### <a name="removewindowsubclass"></a><span data-ttu-id="68a58-161">ремовевиндовсубкласс</span><span class="sxs-lookup"><span data-stu-id="68a58-161">RemoveWindowSubclass</span></span>

<span data-ttu-id="68a58-162">Эта функция удаляет подклассы.</span><span class="sxs-lookup"><span data-stu-id="68a58-162">This function removes subclasses.</span></span> <span data-ttu-id="68a58-163">[**Ремовевиндовсубкласс**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) в сочетании с [**сетвиндовсубкласс**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) позволяет динамически добавлять и удалять подклассы.</span><span class="sxs-lookup"><span data-stu-id="68a58-163">[**RemoveWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-removewindowsubclass) in combination with [**SetWindowSubclass**](/windows/desktop/api/commctrl/nf-commctrl-setwindowsubclass) allows you to dynamically add and remove subclasses.</span></span>

### <a name="defsubclassproc"></a><span data-ttu-id="68a58-164">дефсубкласспрок</span><span class="sxs-lookup"><span data-stu-id="68a58-164">DefSubclassProc</span></span>

<span data-ttu-id="68a58-165">Функция [**дефсубкласспрок**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) вызывает следующий обработчик в цепочке подклассов.</span><span class="sxs-lookup"><span data-stu-id="68a58-165">The [**DefSubclassProc**](/windows/desktop/api/commctrl/nf-commctrl-defsubclassproc) function calls the next handler in the subclass chain.</span></span> <span data-ttu-id="68a58-166">Функция также получает соответствующие ИДЕНТИФИКАТОРы и ссылочные данные и передает их в следующую процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="68a58-166">The function also retrieves the proper ID and reference data and passes the information to the next window procedure.</span></span>

 

 