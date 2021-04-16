---
title: Управление жизненным циклом объекта
description: Узнайте, как управлять жизненным циклом объекта с помощью методов AddRef и Release.
ms.assetid: 0e522ded-8976-4cdd-9a61-eae7834c896b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495e657863150612e5b8efa21fff0b00c7a936b9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/28/2021
ms.locfileid: "104550459"
---
# <a name="managing-the-lifetime-of-an-object"></a><span data-ttu-id="d12d8-103">Управление жизненным циклом объекта</span><span class="sxs-lookup"><span data-stu-id="d12d8-103">Managing the Lifetime of an Object</span></span>

<span data-ttu-id="d12d8-104">Существует правило для COM-интерфейсов, которые еще не упоминались.</span><span class="sxs-lookup"><span data-stu-id="d12d8-104">There is a rule for COM interfaces that we have not yet mentioned.</span></span> <span data-ttu-id="d12d8-105">Каждый COM-интерфейс должен напрямую или косвенно наследовать от интерфейса с именем [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="d12d8-105">Every COM interface must inherit, directly or indirectly, from an interface named [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="d12d8-106">Этот интерфейс предоставляет некоторые базовые возможности, которые должны поддерживаться всеми COM-объектами.</span><span class="sxs-lookup"><span data-stu-id="d12d8-106">This interface provides some baseline capabilities that all COM objects must support.</span></span>

<span data-ttu-id="d12d8-107">Интерфейс [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) определяет три метода:</span><span class="sxs-lookup"><span data-stu-id="d12d8-107">The [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface defines three methods:</span></span>

-   <span data-ttu-id="d12d8-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="d12d8-108">[**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
-   [<span data-ttu-id="d12d8-109">**AddRef**</span><span class="sxs-lookup"><span data-stu-id="d12d8-109">**AddRef**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref)
-   [<span data-ttu-id="d12d8-110">**Release**</span><span class="sxs-lookup"><span data-stu-id="d12d8-110">**Release**</span></span>](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)

<span data-ttu-id="d12d8-111">Метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) позволяет программе запрашивать возможности объекта во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d12d8-111">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method enables a program to query the capabilities of the object at run time.</span></span> <span data-ttu-id="d12d8-112">Мы будем говорить подробнее об этом в следующем разделе, [запросив объект для интерфейса](asking-an-object-for-an-interface.md).</span><span class="sxs-lookup"><span data-stu-id="d12d8-112">We'll say more about that in the next topic, [Asking an Object for an Interface](asking-an-object-for-an-interface.md).</span></span> <span data-ttu-id="d12d8-113">Методы [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) используются для управления временем существования объекта.</span><span class="sxs-lookup"><span data-stu-id="d12d8-113">The [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are used to control the lifetime of an object.</span></span> <span data-ttu-id="d12d8-114">Это тема этого раздела.</span><span class="sxs-lookup"><span data-stu-id="d12d8-114">This is the subject of this topic.</span></span>

## <a name="reference-counting"></a><span data-ttu-id="d12d8-115">Подсчет ссылок</span><span class="sxs-lookup"><span data-stu-id="d12d8-115">Reference Counting</span></span>

<span data-ttu-id="d12d8-116">Независимо от того, что может сделать программа, в некоторый момент она будет распределять и освобождать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d12d8-116">Whatever else a program might do, at some point it will allocate and free resources.</span></span> <span data-ttu-id="d12d8-117">Выделить ресурс несложно.</span><span class="sxs-lookup"><span data-stu-id="d12d8-117">Allocating a resource is easy.</span></span> <span data-ttu-id="d12d8-118">Знание того, когда следует освобождать ресурс, очень сложно, особенно если время существования ресурса выходит за пределы текущей области.</span><span class="sxs-lookup"><span data-stu-id="d12d8-118">Knowing when to free the resource is hard, especially if the lifetime of the resource extends beyond the current scope.</span></span> <span data-ttu-id="d12d8-119">Эта проблема не является уникальной для COM.</span><span class="sxs-lookup"><span data-stu-id="d12d8-119">This problem is not unique to COM.</span></span> <span data-ttu-id="d12d8-120">Любая программа, выделяющая память кучи, должна решить эту же проблему.</span><span class="sxs-lookup"><span data-stu-id="d12d8-120">Any program that allocates heap memory must solve the same problem.</span></span> <span data-ttu-id="d12d8-121">Например, в C++ используются автоматические деструкторы, в то время как C# и Java используют сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="d12d8-121">For example, C++ uses automatic destructors, while C# and Java use garbage collection.</span></span> <span data-ttu-id="d12d8-122">COM использует подход, называемый *подсчетом ссылок*.</span><span class="sxs-lookup"><span data-stu-id="d12d8-122">COM uses an approach called *reference counting*.</span></span>

<span data-ttu-id="d12d8-123">Каждый COM-объект поддерживает внутреннее число.</span><span class="sxs-lookup"><span data-stu-id="d12d8-123">Every COM object maintains an internal count.</span></span> <span data-ttu-id="d12d8-124">Это называется счетчиком ссылок.</span><span class="sxs-lookup"><span data-stu-id="d12d8-124">This is known as the reference count.</span></span> <span data-ttu-id="d12d8-125">Счетчик ссылок отслеживает, сколько ссылок на объект активно в данный момент.</span><span class="sxs-lookup"><span data-stu-id="d12d8-125">The reference count tracks how many references to the object are currently active.</span></span> <span data-ttu-id="d12d8-126">Когда число ссылок становится равным нулю, объект удаляет себя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-126">When the number of references drops to zero, the object deletes itself.</span></span> <span data-ttu-id="d12d8-127">Последняя часть стоит повторять: объект удаляет себя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-127">The last part is worth repeating: The object deletes itself.</span></span> <span data-ttu-id="d12d8-128">Программа никогда не удаляет объект явным образом.</span><span class="sxs-lookup"><span data-stu-id="d12d8-128">The program never explicitly deletes the object.</span></span>

<span data-ttu-id="d12d8-129">Ниже приведены правила для подсчета ссылок.</span><span class="sxs-lookup"><span data-stu-id="d12d8-129">Here are the rules for reference counting:</span></span>

-   <span data-ttu-id="d12d8-130">При первом создании объекта его счетчик ссылок равен 1.</span><span class="sxs-lookup"><span data-stu-id="d12d8-130">When the object is first created, its reference count is 1.</span></span> <span data-ttu-id="d12d8-131">На этом этапе программа имеет один указатель на объект.</span><span class="sxs-lookup"><span data-stu-id="d12d8-131">At this point, the program has a single pointer to the object.</span></span>
-   <span data-ttu-id="d12d8-132">Программа может создать новую ссылку путем дублирования (копирования) указателя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-132">The program can create a new reference by duplicating (copying) the pointer.</span></span> <span data-ttu-id="d12d8-133">При копировании указателя необходимо вызвать метод [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) объекта.</span><span class="sxs-lookup"><span data-stu-id="d12d8-133">When you copy the pointer, you must call the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) method of the object.</span></span> <span data-ttu-id="d12d8-134">Этот метод увеличивает значение счетчика ссылок на единицу.</span><span class="sxs-lookup"><span data-stu-id="d12d8-134">This method increments the reference count by one.</span></span>
-   <span data-ttu-id="d12d8-135">По завершении использования указателя на объект необходимо вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d12d8-135">When you are finished using a pointer to the object, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d12d8-136">Метод **Release** уменьшает значение счетчика ссылок на единицу.</span><span class="sxs-lookup"><span data-stu-id="d12d8-136">The **Release** method decrements the reference count by one.</span></span> <span data-ttu-id="d12d8-137">Он также сделает указатель недействительным.</span><span class="sxs-lookup"><span data-stu-id="d12d8-137">It also invalidates the pointer.</span></span> <span data-ttu-id="d12d8-138">Не используйте указатель снова после вызова **Release**.</span><span class="sxs-lookup"><span data-stu-id="d12d8-138">Do not use the pointer again after you call **Release**.</span></span> <span data-ttu-id="d12d8-139">(При наличии других указателей на один и тот же объект можно продолжать использовать эти указатели.)</span><span class="sxs-lookup"><span data-stu-id="d12d8-139">(If you have other pointers to the same object, you can continue to use those pointers.)</span></span>
-   <span data-ttu-id="d12d8-140">При вызове [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с каждым указателем число ссылок на объект достигает нуля, а сам объект удаляет себя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-140">When you have called [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with every pointer, the object reference count of the object reaches zero, and the object deletes itself.</span></span>

<span data-ttu-id="d12d8-141">На следующей диаграмме показан простой, но типичный вариант.</span><span class="sxs-lookup"><span data-stu-id="d12d8-141">The following diagram shows a simple but typical case.</span></span>

![Схема, на которой показан простой вариант подсчета ссылок.](images/com04.png)

<span data-ttu-id="d12d8-143">Программа создает объект и сохраняет указатель (*p*) в объекте.</span><span class="sxs-lookup"><span data-stu-id="d12d8-143">The program creates an object and stores a pointer (*p*) to the object.</span></span> <span data-ttu-id="d12d8-144">На этом этапе счетчик ссылок равен 1.</span><span class="sxs-lookup"><span data-stu-id="d12d8-144">At this point, the reference count is 1.</span></span> <span data-ttu-id="d12d8-145">Когда программа завершает работу с указателем, она вызывает [**выпуск**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="d12d8-145">When the program is finished using the pointer, it calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="d12d8-146">Счетчик ссылок уменьшается до нуля, и объект удаляет себя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-146">The reference count is decremented to zero, and the object deletes itself.</span></span> <span data-ttu-id="d12d8-147">Now *p* недопустимо.</span><span class="sxs-lookup"><span data-stu-id="d12d8-147">Now *p* is invalid.</span></span> <span data-ttu-id="d12d8-148">Использование *p* для дальнейших вызовов методов является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d12d8-148">It is an error to use *p* for any further method calls.</span></span>

<span data-ttu-id="d12d8-149">На следующей схеме показан более сложный пример.</span><span class="sxs-lookup"><span data-stu-id="d12d8-149">The next diagram shows a more complex example.</span></span>

![Иллюстрация, показывающая подсчет ссылок](images/com05.png)

<span data-ttu-id="d12d8-151">Здесь программа создает объект и сохраняет указатель *p*, как и раньше.</span><span class="sxs-lookup"><span data-stu-id="d12d8-151">Here, the program creates an object and stores the pointer *p*, as before.</span></span> <span data-ttu-id="d12d8-152">Затем программа копирует *p* в новую переменную, *q*.</span><span class="sxs-lookup"><span data-stu-id="d12d8-152">Next, the program copies *p* to a new variable, *q*.</span></span> <span data-ttu-id="d12d8-153">На этом этапе программа должна вызывать [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) для увеличения числа ссылок.</span><span class="sxs-lookup"><span data-stu-id="d12d8-153">At this point, the program must call [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) to increment the reference count.</span></span> <span data-ttu-id="d12d8-154">Теперь число ссылок равно 2, и в объекте есть два допустимых указателя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-154">The reference count is now 2, and there are two valid pointers to the object.</span></span> <span data-ttu-id="d12d8-155">Теперь предположим, что программа завершена с использованием *p*.</span><span class="sxs-lookup"><span data-stu-id="d12d8-155">Now suppose that the program is finished using *p*.</span></span> <span data-ttu-id="d12d8-156">Программа вызывает [**выпуск**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), счетчик ссылок переходит в 1, а *p* больше не действует.</span><span class="sxs-lookup"><span data-stu-id="d12d8-156">The program calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), the reference count goes to 1, and *p* is no longer valid.</span></span> <span data-ttu-id="d12d8-157">Однако *q* остается действительным.</span><span class="sxs-lookup"><span data-stu-id="d12d8-157">However, *q* is still valid.</span></span> <span data-ttu-id="d12d8-158">Позже программа завершит использование *q*.</span><span class="sxs-lookup"><span data-stu-id="d12d8-158">Later, the program finishes using *q*.</span></span> <span data-ttu-id="d12d8-159">Поэтому он снова вызывает метод **Release** .</span><span class="sxs-lookup"><span data-stu-id="d12d8-159">Therefore, it calls **Release** again.</span></span> <span data-ttu-id="d12d8-160">Число ссылок становится равным нулю, а объект удаляет себя.</span><span class="sxs-lookup"><span data-stu-id="d12d8-160">The reference count goes to zero, and the object deletes itself.</span></span>

<span data-ttu-id="d12d8-161">Может возникнуть вопрос, почему программа скопирует *p*.</span><span class="sxs-lookup"><span data-stu-id="d12d8-161">You might wonder why the program would copy *p*.</span></span> <span data-ttu-id="d12d8-162">Есть две основные причины: сначала может потребоваться сохранить указатель в структуре данных, например в списке.</span><span class="sxs-lookup"><span data-stu-id="d12d8-162">There are two main reasons: First, you might want to store the pointer in a data structure, such as a list.</span></span> <span data-ttu-id="d12d8-163">Во вторых, может потребоваться, чтобы указатель оставался за пределами текущей области исходной переменной.</span><span class="sxs-lookup"><span data-stu-id="d12d8-163">Second, you might want to keep the pointer beyond the current scope of the original variable.</span></span> <span data-ttu-id="d12d8-164">Поэтому его нужно скопировать в новую переменную с более широкими областями.</span><span class="sxs-lookup"><span data-stu-id="d12d8-164">Therefore, you would copy it to a new variable with wider scope.</span></span>

<span data-ttu-id="d12d8-165">Одним из преимуществ подсчета ссылок является то, что вы можете совместно использовать указатели в разных разделах кода, не используя разные пути кода для удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="d12d8-165">One advantage of reference counting is that you can share pointers across different sections of code, without the various code paths coordinating to delete the object.</span></span> <span data-ttu-id="d12d8-166">Вместо этого каждый путь кода просто вызывает метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , когда этот путь кода выполняется с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="d12d8-166">Instead, each code path merely calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when that code path is done using the object.</span></span> <span data-ttu-id="d12d8-167">Объект обрабатывает сам себя в нужное время.</span><span class="sxs-lookup"><span data-stu-id="d12d8-167">The object handles deleting itself at the correct time.</span></span>

## <a name="example"></a><span data-ttu-id="d12d8-168">Пример</span><span class="sxs-lookup"><span data-stu-id="d12d8-168">Example</span></span>

<span data-ttu-id="d12d8-169">Ниже приведен код из [примера открытия диалогового окна](example--the-open-dialog-box.md) .</span><span class="sxs-lookup"><span data-stu-id="d12d8-169">Here is the code from the [Open dialog box example](example--the-open-dialog-box.md) again.</span></span>

```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    IFileOpenDialog *pFileOpen;

    hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL,
            IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(NULL);
        if (SUCCEEDED(hr))
        {
            IShellItem *pItem;
            hr = pFileOpen->GetResult(&pItem);
            if (SUCCEEDED(hr))
            {
                PWSTR pszFilePath;
                hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);
                if (SUCCEEDED(hr))
                {
                    MessageBox(NULL, pszFilePath, L&quot;File Path&quot;, MB_OK);
                    CoTaskMemFree(pszFilePath);
                }
                pItem->Release();
            }
        }
        pFileOpen->Release();
    }
    CoUninitialize();
}
````

<span data-ttu-id="d12d8-170">Подсчет ссылок выполняется в двух местах этого кода.</span><span class="sxs-lookup"><span data-stu-id="d12d8-170">Reference counting occurs in two places in this code.</span></span> <span data-ttu-id="d12d8-171">Во первых, если программа успешно создает объект диалогового окна общего элемента, он должен вызвать [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) для указателя *пфилеопен* .</span><span class="sxs-lookup"><span data-stu-id="d12d8-171">First, if program successfully creates the Common Item Dialog object, it must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pFileOpen* pointer.</span></span>

```C++
hr = CoCreateInstance(CLSID_FileOpenDialog, NULL, CLSCTX_ALL, 
        IID_IFileOpenDialog, reinterpret_cast<void**>(&pFileOpen));

if (SUCCEEDED(hr))
{
    // ...
    pFileOpen->Release();
}
```

<span data-ttu-id="d12d8-172">Во-вторых, [**когда метод**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) [**интерфейса IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) возвращает указатель на интерфейс, программа должна вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) для указателя *питем* .</span><span class="sxs-lookup"><span data-stu-id="d12d8-172">Second, when the [**GetResult**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) method returns a pointer to the [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) interface, the program must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on the *pItem* pointer.</span></span>

```C++
hr = pFileOpen->GetResult(&pItem);

if (SUCCEEDED(hr))
{
    // ...
    pItem->Release();
}
```

<span data-ttu-id="d12d8-173">Обратите внимание, что в обоих случаях вызов [**выпуска**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) является последним, который происходит перед тем, как указатель выходит из области действия.</span><span class="sxs-lookup"><span data-stu-id="d12d8-173">Notice that in both cases, the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) call is the last thing that happens before the pointer goes out of scope.</span></span> <span data-ttu-id="d12d8-174">Также обратите внимание, что метод **Release** вызывается только после проверки **значения HRESULT** на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="d12d8-174">Also notice that **Release** is called only after you test the **HRESULT** for success.</span></span> <span data-ttu-id="d12d8-175">Например, если вызов [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) завершается ошибкой, то указатель *пфилеопен* является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d12d8-175">For example, if the call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails, the *pFileOpen* pointer is not valid.</span></span> <span data-ttu-id="d12d8-176">Поэтому вызов метода **Release** с указателем будет ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d12d8-176">Therefore, it would be an error to call **Release** on the pointer.</span></span>

## <a name="next"></a><span data-ttu-id="d12d8-177">Следующая</span><span class="sxs-lookup"><span data-stu-id="d12d8-177">Next</span></span>

[<span data-ttu-id="d12d8-178">Запрос объекта для интерфейса</span><span class="sxs-lookup"><span data-stu-id="d12d8-178">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)