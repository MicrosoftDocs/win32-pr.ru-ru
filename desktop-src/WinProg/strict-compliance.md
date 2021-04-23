---
title: ЖЕСТКОЕ соответствие
description: При включении СТРОГОй проверки типов часть исходного кода, который успешно компилируется, может выдавать сообщения об ошибках.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413225"
---
# <a name="strict-compliance"></a><span data-ttu-id="0197a-103">ЖЕСТКОЕ соответствие</span><span class="sxs-lookup"><span data-stu-id="0197a-103">STRICT Compliance</span></span>

<span data-ttu-id="0197a-104">При включении **строгой** проверки типов часть исходного кода, который успешно компилируется, может выдавать сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0197a-104">Some source code that compiles successfully might produce error messages when you enable **STRICT** type checking.</span></span> <span data-ttu-id="0197a-105">В следующих разделах описаны минимальные требования к компиляции кода при включенном параметре **On** .</span><span class="sxs-lookup"><span data-stu-id="0197a-105">The following sections describe the minimal requirements for making your code compile when **STRICT** is enabled.</span></span> <span data-ttu-id="0197a-106">Рекомендуется выполнить дополнительные действия, особенно для создания переносимого кода.</span><span class="sxs-lookup"><span data-stu-id="0197a-106">Additional steps are recommended, especially to produce portable code.</span></span>

## <a name="general-requirements"></a><span data-ttu-id="0197a-107">Общие требования</span><span class="sxs-lookup"><span data-stu-id="0197a-107">General Requirements</span></span>

<span data-ttu-id="0197a-108">Основное требование заключается в том, что необходимо объявить правильные типы обработчиков и указатели функций вместо того, чтобы полагаться на более общие типы.</span><span class="sxs-lookup"><span data-stu-id="0197a-108">The principal requirement is that you must declare correct handle types and function pointers instead of relying on more general types.</span></span> <span data-ttu-id="0197a-109">Нельзя использовать один тип обработчика, где ожидается другой.</span><span class="sxs-lookup"><span data-stu-id="0197a-109">You cannot use one handle type where another is expected.</span></span> <span data-ttu-id="0197a-110">Это также означает, что может потребоваться изменить объявления функций и использовать дополнительные приведения типов.</span><span class="sxs-lookup"><span data-stu-id="0197a-110">This also means that you may have to change function declarations and use more type casts.</span></span>

<span data-ttu-id="0197a-111">Для достижения лучших результатов тип универсального **маркера** следует использовать только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0197a-111">For best results, the generic **HANDLE** type should be used only when necessary.</span></span>

## <a name="declaring-functions-within-your-application"></a><span data-ttu-id="0197a-112">Объявление функций в приложении</span><span class="sxs-lookup"><span data-stu-id="0197a-112">Declaring Functions Within Your Application</span></span>

<span data-ttu-id="0197a-113">Убедитесь, что объявлены все функции приложения.</span><span class="sxs-lookup"><span data-stu-id="0197a-113">Make sure all application functions are declared.</span></span> <span data-ttu-id="0197a-114">Рекомендуется размещать все объявления функций в включаемом файле, так как вы можете легко проверить объявления и найти параметры и возвращаемые типы, которые следует изменить.</span><span class="sxs-lookup"><span data-stu-id="0197a-114">Placing all function declarations in an include file is recommended because you can easily scan your declarations and look for parameter and return types that should be changed.</span></span>

<span data-ttu-id="0197a-115">При использовании параметра компилятора **/Zg** для создания файлов заголовков для функций следует помнить, что результаты будут разными, в зависимости от того, включена ли **строго** проверка типов.</span><span class="sxs-lookup"><span data-stu-id="0197a-115">If you use the **/Zg** compiler option to create header files for your functions, remember that you will get different results depending on whether you have enabled **STRICT** type checking.</span></span> <span data-ttu-id="0197a-116">При использовании **строгого** отключения все типы обработчиков создают один и тот же базовый тип.</span><span class="sxs-lookup"><span data-stu-id="0197a-116">With **STRICT** disabled, all handle types generate the same base type.</span></span> <span data-ttu-id="0197a-117">При **использовании требований** с поддержкой определенных типов они создают разные базовые типы.</span><span class="sxs-lookup"><span data-stu-id="0197a-117">With **STRICT** enabled, they generate different base types.</span></span> <span data-ttu-id="0197a-118">Чтобы избежать **конфликта, необходимо** повторно создать файл заголовка каждый раз при включении или отключении или изменении файла заголовка для использования типов **HWND**, **HDC**, **Handle** и т. д. вместо базовых типов.</span><span class="sxs-lookup"><span data-stu-id="0197a-118">To avoid conflict, you need to re-create the header file each time you enable or disable **STRICT**, or edit the header file to use the types **HWND**, **HDC**, **HANDLE**, and so on, instead of the base types.</span></span>

<span data-ttu-id="0197a-119">Все объявления функций, скопированные из Windows. h в исходный код, могли быть изменены, а локальное объявление может устареть.</span><span class="sxs-lookup"><span data-stu-id="0197a-119">Any function declarations that you copied from Windows.h into your source code may have changed, and your local declaration may be out of date.</span></span> <span data-ttu-id="0197a-120">Удалите локальное объявление.</span><span class="sxs-lookup"><span data-stu-id="0197a-120">Remove your local declaration.</span></span>

## <a name="types-that-require-casts"></a><span data-ttu-id="0197a-121">Типы, для которых требуются приведения</span><span class="sxs-lookup"><span data-stu-id="0197a-121">Types that Require Casts</span></span>

<span data-ttu-id="0197a-122">Некоторые функции имеют универсальные типы возвращаемых значения или параметры.</span><span class="sxs-lookup"><span data-stu-id="0197a-122">Some functions have generic return types or parameters.</span></span> <span data-ttu-id="0197a-123">Например, функция [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) возвращает данные, которые могут быть любого числа типов, в зависимости от контекста.</span><span class="sxs-lookup"><span data-stu-id="0197a-123">For example, the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function returns data that may be any number of types, depending on the context.</span></span> <span data-ttu-id="0197a-124">Если в исходном коде отображаются какие-либо из этих функций, убедитесь, что используется правильная операция приведения типов и что это возможно.</span><span class="sxs-lookup"><span data-stu-id="0197a-124">When you see any of these functions in your source code, make sure that you use the correct type cast and that it is as specific as possible.</span></span> <span data-ttu-id="0197a-125">В следующем списке приведен пример этих функций.</span><span class="sxs-lookup"><span data-stu-id="0197a-125">The following list is an example of these functions.</span></span>

-   [<span data-ttu-id="0197a-126">**локаллокк**</span><span class="sxs-lookup"><span data-stu-id="0197a-126">**LocalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [<span data-ttu-id="0197a-127">**GlobalLock**</span><span class="sxs-lookup"><span data-stu-id="0197a-127">**GlobalLock**</span></span>](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [<span data-ttu-id="0197a-128">**жетвиндовлонг**</span><span class="sxs-lookup"><span data-stu-id="0197a-128">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [<span data-ttu-id="0197a-129">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="0197a-129">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [<span data-ttu-id="0197a-130">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="0197a-130">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [<span data-ttu-id="0197a-131">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="0197a-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [<span data-ttu-id="0197a-132">**сенддлгитеммессаже**</span><span class="sxs-lookup"><span data-stu-id="0197a-132">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

<span data-ttu-id="0197a-133">При вызове [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)или [**сенддлгитеммессаже**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)сначала следует привести результат к типу **uint \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="0197a-133">When you call [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), or [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea), you should first cast the result to type **UINT\_PTR**.</span></span> <span data-ttu-id="0197a-134">Необходимо выполнить аналогичные действия для любой функции, возвращающей значение **\_ типа** **lResult** или long, где результат содержит маркер.</span><span class="sxs-lookup"><span data-stu-id="0197a-134">You need to take similar steps for any function that returns an **LRESULT** or **LONG\_PTR** value, where the result contains a handle.</span></span> <span data-ttu-id="0197a-135">Это необходимо для написания переносимого кода, так как размер маркера зависит от версии Windows.</span><span class="sxs-lookup"><span data-stu-id="0197a-135">This is necessary for writing portable code because the size of a handle varies, depending on the version of Windows.</span></span> <span data-ttu-id="0197a-136">Приведение **\_ типа uint PTR** обеспечивает правильное преобразование.</span><span class="sxs-lookup"><span data-stu-id="0197a-136">The (**UINT\_PTR**) cast ensures proper conversion.</span></span> <span data-ttu-id="0197a-137">В следующем коде показан пример, в котором **SendMessage** возвращает дескриптор кисти:</span><span class="sxs-lookup"><span data-stu-id="0197a-137">The following code shows an example in which **SendMessage** returns a handle to a brush:</span></span>


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



<span data-ttu-id="0197a-138">Параметр **CreateWindow** и **CreateWindowEx** *HMENU* иногда используется для передачи идентификатора элемента управления целочисленного типа (ID).</span><span class="sxs-lookup"><span data-stu-id="0197a-138">The **CreateWindow** and **CreateWindowEx** parameter *hmenu* is sometimes used to pass an integer control identifier (ID).</span></span> <span data-ttu-id="0197a-139">В этом случае необходимо привести идентификатор к типу **HMENU** :</span><span class="sxs-lookup"><span data-stu-id="0197a-139">In this case, you must cast the ID to an **HMENU** type:</span></span>


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a><span data-ttu-id="0197a-140">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0197a-140">Additional Considerations</span></span>

<span data-ttu-id="0197a-141">Чтобы получить максимальную пользу от **строгой** проверки типов, необходимо следовать дополнительным рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="0197a-141">To get the most benefit from **STRICT** type checking, there are additional guidelines you should follow.</span></span> <span data-ttu-id="0197a-142">В будущих версиях Windows код будет более переносимым, если вы внесете следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="0197a-142">Your code will be more portable in future versions of Windows if you make the following changes.</span></span>

<span data-ttu-id="0197a-143">Типы **wParam**, **lParam**, **lResult** и **лпвоид** — это *типы данных с полиморфизмом*.</span><span class="sxs-lookup"><span data-stu-id="0197a-143">The types **WPARAM**, **LPARAM**, **LRESULT**, and **LPVOID** are *polymorphic data types*.</span></span> <span data-ttu-id="0197a-144">Они хранят различные виды данных в разное время, даже если включена **строго** проверка типов.</span><span class="sxs-lookup"><span data-stu-id="0197a-144">They hold different kinds of data at different times, even when **STRICT** type checking is enabled.</span></span> <span data-ttu-id="0197a-145">Чтобы получить преимущества проверки типов, необходимо как можно быстрее привести значения этих типов.</span><span class="sxs-lookup"><span data-stu-id="0197a-145">To get the benefit of type checking, you should cast values of these types as soon as possible.</span></span> <span data-ttu-id="0197a-146">(Обратите внимание, что средство взлома сообщений автоматически переводит *wParam* и *lParam* в переносимом виде.)</span><span class="sxs-lookup"><span data-stu-id="0197a-146">(Note that message crackers automatically recast *wParam* and *lParam* for you in a portable way.)</span></span>

<span data-ttu-id="0197a-147">Соблюдайте особое внимание, чтобы различать типы **хмодуле** и **HINSTANCE** .</span><span class="sxs-lookup"><span data-stu-id="0197a-147">Take special care to distinguish **HMODULE** and **HINSTANCE** types.</span></span> <span data-ttu-id="0197a-148">Даже при **строгом** включении они определяются как один и тот же базовый тип.</span><span class="sxs-lookup"><span data-stu-id="0197a-148">Even with **STRICT** enabled, they are defined as the same base type.</span></span> <span data-ttu-id="0197a-149">Большинство функций управления модулями ядра используют типы **HINSTANCE** , но существует несколько функций, которые возвращают или принимают только типы **хмодуле** .</span><span class="sxs-lookup"><span data-stu-id="0197a-149">Most kernel module management functions use **HINSTANCE** types, but there are a few functions that return or accept only **HMODULE** types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0197a-150">См. также</span><span class="sxs-lookup"><span data-stu-id="0197a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0197a-151">Отключение</span><span class="sxs-lookup"><span data-stu-id="0197a-151">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="0197a-152">Включение параметра</span><span class="sxs-lookup"><span data-stu-id="0197a-152">Enabling STRICT</span></span>](enabling-strict.md)
</dt> </dl>

 

 