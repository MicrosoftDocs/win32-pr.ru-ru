---
title: Методики программирования COM
description: В этом разделе описываются способы повышения эффективности и надежности кода COM.
ms.assetid: 76aca556-b4d6-4e67-a2a3-4439900f0c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26143e5049c3db7efcbcc9353e74890fe0009c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104134711"
---
# <a name="com-coding-practices"></a><span data-ttu-id="33fd8-103">Методики программирования COM</span><span class="sxs-lookup"><span data-stu-id="33fd8-103">COM Coding Practices</span></span>

<span data-ttu-id="33fd8-104">В этом разделе описываются способы повышения эффективности и надежности кода COM.</span><span class="sxs-lookup"><span data-stu-id="33fd8-104">This topic describes ways to make your COM code more effective and robust.</span></span>

-   [<span data-ttu-id="33fd8-105">\_ \_ Оператор ууидоф</span><span class="sxs-lookup"><span data-stu-id="33fd8-105">The \_\_uuidof Operator</span></span>](/windows)
-   [<span data-ttu-id="33fd8-106">Макрос IID \_ ППВ \_ args</span><span class="sxs-lookup"><span data-stu-id="33fd8-106">The IID\_PPV\_ARGS Macro</span></span>](/windows)
-   [<span data-ttu-id="33fd8-107">Шаблон Саферелеасе</span><span class="sxs-lookup"><span data-stu-id="33fd8-107">The SafeRelease Pattern</span></span>](#the-saferelease-pattern)
-   [<span data-ttu-id="33fd8-108">Интеллектуальные указатели COM</span><span class="sxs-lookup"><span data-stu-id="33fd8-108">COM Smart Pointers</span></span>](#com-smart-pointers)

## <a name="the-__uuidof-operator"></a><span data-ttu-id="33fd8-109">\_ \_ Оператор ууидоф</span><span class="sxs-lookup"><span data-stu-id="33fd8-109">The \_\_uuidof Operator</span></span>

<span data-ttu-id="33fd8-110">При сборке программы могут возникать ошибки компоновщика, аналогичные следующим:</span><span class="sxs-lookup"><span data-stu-id="33fd8-110">When you build your program, you might get linker errors similar to the following:</span></span>

`unresolved external symbol "struct _GUID const IID_IDrawable"`

<span data-ttu-id="33fd8-111">Эта ошибка означает, что константа GUID была объявлена с внешней компоновкой (**extern**), и компоновщику не удалось найти определение константы.</span><span class="sxs-lookup"><span data-stu-id="33fd8-111">This error means that a GUID constant was declared with external linkage (**extern**), and the linker could not find the definition of the constant.</span></span> <span data-ttu-id="33fd8-112">Значение константы GUID обычно экспортируется из файла статической библиотеки.</span><span class="sxs-lookup"><span data-stu-id="33fd8-112">The value of a GUID constant is usually exported from a static library file.</span></span> <span data-ttu-id="33fd8-113">При использовании Microsoft Visual C++ можно избежать необходимости связывать статическую библиотеку с помощью оператора **\_ \_ ууидоф** .</span><span class="sxs-lookup"><span data-stu-id="33fd8-113">If you are using Microsoft Visual C++, you can avoid the need to link a static library by using the **\_\_uuidof** operator.</span></span> <span data-ttu-id="33fd8-114">Этот оператор является расширением языка Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="33fd8-114">This operator is a Microsoft language extension.</span></span> <span data-ttu-id="33fd8-115">Он возвращает значение идентификатора GUID из выражения.</span><span class="sxs-lookup"><span data-stu-id="33fd8-115">It returns a GUID value from an expression.</span></span> <span data-ttu-id="33fd8-116">Выражение может быть именем типа интерфейса, именем класса или указателем интерфейса.</span><span class="sxs-lookup"><span data-stu-id="33fd8-116">The expression can be an interface type name, a class name, or an interface pointer.</span></span> <span data-ttu-id="33fd8-117">С помощью **\_ \_ ууидоф** можно создать объект диалогового окна общего элемента следующим образом:</span><span class="sxs-lookup"><span data-stu-id="33fd8-117">Using **\_\_uuidof**, you can create the Common Item Dialog object as follows:</span></span>


```C++
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    __uuidof(pFileOpen), reinterpret_cast<void**>(&pFileOpen));
```



<span data-ttu-id="33fd8-118">Компилятор извлекает значение идентификатора GUID из заголовка, поэтому экспорт библиотеки не требуется.</span><span class="sxs-lookup"><span data-stu-id="33fd8-118">The compiler extracts the GUID value from the header, so no library export is necessary.</span></span>

> [!Note]  
> <span data-ttu-id="33fd8-119">Значение идентификатора GUID связывается с именем типа путем объявления `__declspec(uuid( ... ))` в заголовке.</span><span class="sxs-lookup"><span data-stu-id="33fd8-119">The GUID value is associated with the type name by declaring `__declspec(uuid( ... ))` in the header.</span></span> <span data-ttu-id="33fd8-120">Дополнительные сведения см. в документации по **\_ \_ declspec** в документации по Visual C++.</span><span class="sxs-lookup"><span data-stu-id="33fd8-120">For more information, see the documentation for **\_\_declspec** in the Visual C++ documentation.</span></span>

 

## <a name="the-iid_ppv_args-macro"></a><span data-ttu-id="33fd8-121">Макрос IID \_ ППВ \_ args</span><span class="sxs-lookup"><span data-stu-id="33fd8-121">The IID\_PPV\_ARGS Macro</span></span>

<span data-ttu-id="33fd8-122">Мы видели, что методы [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) и [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) нуждаются в преобразовании финального параметра в **тип \* \* void** .</span><span class="sxs-lookup"><span data-stu-id="33fd8-122">We saw that both [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) require coercing the final parameter to a **void\*\*** type.</span></span> <span data-ttu-id="33fd8-123">Это создает потенциал для несоответствия типов.</span><span class="sxs-lookup"><span data-stu-id="33fd8-123">This creates the potential for a type mismatch.</span></span> <span data-ttu-id="33fd8-124">Рассмотрим следующий фрагмент кода:</span><span class="sxs-lookup"><span data-stu-id="33fd8-124">Consider the following code fragment:</span></span>


```C++
// Wrong!

IFileOpenDialog *pFileOpen;

hr = CoCreateInstance(
    __uuidof(FileOpenDialog), 
    NULL, 
    CLSCTX_ALL, 
    __uuidof(IFileDialogCustomize),       // The IID does not match the pointer type!
    reinterpret_cast<void**>(&pFileOpen)  // Coerce to void**.
    );
```



<span data-ttu-id="33fd8-125">Этот код запрашивает интерфейс [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , но передается в указатель [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="33fd8-125">This code asks for the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface, but passes in an [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer.</span></span> <span data-ttu-id="33fd8-126">Выражение **\_ приведения переинтерпретации** обходит систему типов C++, поэтому компилятор не будет перехватывать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="33fd8-126">The **reinterpret\_cast** expression circumvents the C++ type system, so the compiler will not catch this error.</span></span> <span data-ttu-id="33fd8-127">В лучшем случае, если объект не реализует запрошенный интерфейс, вызов просто завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="33fd8-127">In the best case, if the object does not implement the requested interface, the call simply fails.</span></span> <span data-ttu-id="33fd8-128">В худшем случае функция выполняется успешно и имеется несовпадающий указатель.</span><span class="sxs-lookup"><span data-stu-id="33fd8-128">In the worst case, the function succeeds and you have a mismatched pointer.</span></span> <span data-ttu-id="33fd8-129">Иными словами, тип указателя не соответствует фактической таблице vtable в памяти.</span><span class="sxs-lookup"><span data-stu-id="33fd8-129">In other words, the pointer type does not match the actual vtable in memory.</span></span> <span data-ttu-id="33fd8-130">Как можно себе представить, на этом этапе ничего не может произойти.</span><span class="sxs-lookup"><span data-stu-id="33fd8-130">As you can imagine, nothing good can happen at that point.</span></span>

> [!Note]  
> <span data-ttu-id="33fd8-131">Таблица виртуальных методов ( *vtable* ) — это таблица указателей на функции.</span><span class="sxs-lookup"><span data-stu-id="33fd8-131">A *vtable* (virtual method table) is a table of function pointers.</span></span> <span data-ttu-id="33fd8-132">Таблица vtable заключается в том, как COM привязывает вызов метода к его реализации во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="33fd8-132">The vtable is how COM binds a method call to its implementation at run time.</span></span> <span data-ttu-id="33fd8-133">Некстати, таблицы vtable — это то, как большинство компиляторов C++ реализуют виртуальные методы.</span><span class="sxs-lookup"><span data-stu-id="33fd8-133">Not coincidentally, vtables are how most C++ compilers implement virtual methods.</span></span>

 

<span data-ttu-id="33fd8-134">Макрос [**IID \_ ППВ \_ argss**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) помогает избежать этого класса ошибки.</span><span class="sxs-lookup"><span data-stu-id="33fd8-134">The [**IID\_PPV\_ARGS**](/windows/desktop/api/combaseapi/nf-combaseapi-iid_ppv_args) macro helps to avoid this class of error.</span></span> <span data-ttu-id="33fd8-135">Чтобы использовать этот макрос, замените следующий код:</span><span class="sxs-lookup"><span data-stu-id="33fd8-135">To use this macro, replace the following code:</span></span>


```C++
__uuidof(IFileDialogCustomize), reinterpret_cast<void**>(&pFileOpen)
```



<span data-ttu-id="33fd8-136">следующим кодом:</span><span class="sxs-lookup"><span data-stu-id="33fd8-136">with this:</span></span>


```C++
IID_PPV_ARGS(&pFileOpen)
```



<span data-ttu-id="33fd8-137">Макрос автоматически вставляет `__uuidof(IFileOpenDialog)` идентификатор интерфейса, поэтому он гарантированно соответствует типу указателя.</span><span class="sxs-lookup"><span data-stu-id="33fd8-137">The macro automatically inserts `__uuidof(IFileOpenDialog)` for the interface identifier, so it is guaranteed to match the pointer type.</span></span> <span data-ttu-id="33fd8-138">Ниже приведен измененный (и правильный) код.</span><span class="sxs-lookup"><span data-stu-id="33fd8-138">Here is the modified (and correct) code:</span></span>


```C++
// Right.
IFileOpenDialog *pFileOpen;
hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, CLSCTX_ALL, 
    IID_PPV_ARGS(&pFileOpen));
```



<span data-ttu-id="33fd8-139">Один и тот же макрос можно использовать с [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="33fd8-139">You can use the same macro with [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>


```C++
IFileDialogCustomize *pCustom;
hr = pFileOpen->QueryInterface(IID_PPV_ARGS(&pCustom));
```



## <a name="the-saferelease-pattern"></a><span data-ttu-id="33fd8-140">Шаблон Саферелеасе</span><span class="sxs-lookup"><span data-stu-id="33fd8-140">The SafeRelease Pattern</span></span>

<span data-ttu-id="33fd8-141">Подсчет ссылок — это одна из тех вещей в программировании, которая, по сути, проста, но она также утомительна, что позволяет легко получить ошибку.</span><span class="sxs-lookup"><span data-stu-id="33fd8-141">Reference counting is one of those things in programming that is basically easy, but is also tedious, which makes it easy to get wrong.</span></span> <span data-ttu-id="33fd8-142">Типовые ошибки включают:</span><span class="sxs-lookup"><span data-stu-id="33fd8-142">Typical errors include:</span></span>

-   <span data-ttu-id="33fd8-143">Не удается освободить указатель интерфейса по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="33fd8-143">Failing to release an interface pointer when you are done using it.</span></span> <span data-ttu-id="33fd8-144">Этот класс ошибок приведет к утечке памяти программой и другим ресурсам, так как объекты не уничтожаются.</span><span class="sxs-lookup"><span data-stu-id="33fd8-144">This class of bug will cause your program to leak memory and other resources, because objects are not destroyed.</span></span>
-   <span data-ttu-id="33fd8-145">Вызов [**выпуска**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с недопустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="33fd8-145">Calling [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) with an invalid pointer.</span></span> <span data-ttu-id="33fd8-146">Например, эта ошибка может произойти, если объект не был создан.</span><span class="sxs-lookup"><span data-stu-id="33fd8-146">For example, this error can happen if the object was never created.</span></span> <span data-ttu-id="33fd8-147">Эта категория ошибок, вероятно, приведет к сбою программы.</span><span class="sxs-lookup"><span data-stu-id="33fd8-147">This category of bug will probably cause your program to crash.</span></span>
-   <span data-ttu-id="33fd8-148">Разыменование указателя интерфейса после вызова метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="33fd8-148">Dereferencing an interface pointer after [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) is called.</span></span> <span data-ttu-id="33fd8-149">Эта ошибка может привести к сбою программы.</span><span class="sxs-lookup"><span data-stu-id="33fd8-149">This bug may cause your program to crash.</span></span> <span data-ttu-id="33fd8-150">Что еще хуже, это может привести к сбою программы в случайном будущем, что затрудняет отслеживание исходной ошибки.</span><span class="sxs-lookup"><span data-stu-id="33fd8-150">Worse, it may cause your program to crash at a random later time, making it hard to track down the original error.</span></span>

<span data-ttu-id="33fd8-151">Одним из способов избежать этих ошибок является вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) с помощью функции, которая безопасно освобождает указатель.</span><span class="sxs-lookup"><span data-stu-id="33fd8-151">One way to avoid these bugs is to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) through a function that safely releases the pointer.</span></span> <span data-ttu-id="33fd8-152">В следующем коде показана функция, которая делает следующее:</span><span class="sxs-lookup"><span data-stu-id="33fd8-152">The following code shows a function that does this:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



<span data-ttu-id="33fd8-153">Эта функция принимает указатель COM-интерфейса в качестве параметра и выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="33fd8-153">This function takes a COM interface pointer as a parameter and does the following:</span></span>

1.  <span data-ttu-id="33fd8-154">Проверяет, имеет ли указатель **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-154">Checks whether the pointer is **NULL**.</span></span>
2.  <span data-ttu-id="33fd8-155">Вызывает метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , если указатель не имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-155">Calls [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) if the pointer is not **NULL**.</span></span>
3.  <span data-ttu-id="33fd8-156">Устанавливает указатель на **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-156">Sets the pointer to **NULL**.</span></span>

<span data-ttu-id="33fd8-157">Ниже приведен пример использования `SafeRelease` :</span><span class="sxs-lookup"><span data-stu-id="33fd8-157">Here is an example of how to use `SafeRelease`:</span></span>


```C++
void UseSafeRelease()
{
    IFileOpenDialog *pFileOpen = NULL;

    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        // Use the object.
    }
    SafeRelease(&pFileOpen);
}
```



<span data-ttu-id="33fd8-158">Если [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) выполнен, вызов `SafeRelease` освобождает указатель.</span><span class="sxs-lookup"><span data-stu-id="33fd8-158">If [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) succeeds, the call to `SafeRelease` releases the pointer.</span></span> <span data-ttu-id="33fd8-159">Если **CoCreateInstance** завершается ошибкой, *пфилеопен* остается **пустым**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-159">If **CoCreateInstance** fails, *pFileOpen* remains **NULL**.</span></span> <span data-ttu-id="33fd8-160">`SafeRelease`Функция проверяет наличие этого и пропускает вызов метода [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="33fd8-160">The `SafeRelease` function checks for this and skips the call to [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span>

<span data-ttu-id="33fd8-161">Также можно вызвать `SafeRelease` более одного раза в одном и том же указателе, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="33fd8-161">It is also safe to call `SafeRelease` more than once on the same pointer, as shown here:</span></span>


```C++
// Redundant, but OK.
SafeRelease(&pFileOpen);
SafeRelease(&pFileOpen);
```



## <a name="com-smart-pointers"></a><span data-ttu-id="33fd8-162">Интеллектуальные указатели COM</span><span class="sxs-lookup"><span data-stu-id="33fd8-162">COM Smart Pointers</span></span>

<span data-ttu-id="33fd8-163">`SafeRelease`Функция полезна, но требует запоминать две вещи:</span><span class="sxs-lookup"><span data-stu-id="33fd8-163">The `SafeRelease` function is useful, but it requires you to remember two things:</span></span>

-   <span data-ttu-id="33fd8-164">Инициализируйте каждый указатель интерфейса на **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-164">Initialize every interface pointer to **NULL**.</span></span>
-   <span data-ttu-id="33fd8-165">Вызовите, `SafeRelease` прежде чем каждый указатель выходит за пределы области.</span><span class="sxs-lookup"><span data-stu-id="33fd8-165">Call `SafeRelease` before each pointer goes out of scope.</span></span>

<span data-ttu-id="33fd8-166">Как программист на C++, вы, вероятно, думаете, что вам не нужно запоминать ни одно из этих вещей.</span><span class="sxs-lookup"><span data-stu-id="33fd8-166">As a C++ programmer, you are probably thinking that you shouldn't have to remember either of these things.</span></span> <span data-ttu-id="33fd8-167">В конце концов, вот почему C++ имеет конструкторы и деструкторы.</span><span class="sxs-lookup"><span data-stu-id="33fd8-167">After all, that's why C++ has constructors and destructors.</span></span> <span data-ttu-id="33fd8-168">Было бы неплохо иметь класс, который заключает указатель базового интерфейса и автоматически инициализирует и освобождает указатель.</span><span class="sxs-lookup"><span data-stu-id="33fd8-168">It would be nice to have a class that wraps the underlying interface pointer and automatically initializes and releases the pointer.</span></span> <span data-ttu-id="33fd8-169">Другими словами, нам нужно нечто вроде этого:</span><span class="sxs-lookup"><span data-stu-id="33fd8-169">In other words, we want something like this:</span></span>


```C++
// Warning: This example is not complete.

template <class T>
class SmartPointer
{
    T* ptr;

 public:
    SmartPointer(T *p) : ptr(p) { }
    ~SmartPointer()
    {
        if (ptr) { ptr->Release(); }
    }
};
```



<span data-ttu-id="33fd8-170">Приведенное здесь определение класса является неполным и не может использоваться, как показано.</span><span class="sxs-lookup"><span data-stu-id="33fd8-170">The class definition shown here is incomplete, and is not usable as shown.</span></span> <span data-ttu-id="33fd8-171">Как минимум необходимо определить конструктор копии, оператор присваивания и способ доступа к базовому указателю COM.</span><span class="sxs-lookup"><span data-stu-id="33fd8-171">At a minimum, you would need to define a copy constructor, an assignment operator, and a way to access the underlying COM pointer.</span></span> <span data-ttu-id="33fd8-172">К счастью, вам не нужно выполнять какую-либо из этих действий, поскольку Microsoft Visual Studio уже предоставляет класс интеллектуального указателя как часть библиотеки ATL.</span><span class="sxs-lookup"><span data-stu-id="33fd8-172">Fortunately, you don't need to do any of this work, because Microsoft Visual Studio already provides a smart pointer class as part of the Active Template Library (ATL).</span></span>

<span data-ttu-id="33fd8-173">Класс интеллектуального указателя ATL называется **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-173">The ATL smart pointer class is named **CComPtr**.</span></span> <span data-ttu-id="33fd8-174">(Существует также класс **CComQIPtr** , который здесь не рассматривается.) Ниже приведен пример [открытого диалогового окна](example--the-open-dialog-box.md) , в котором используется **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="33fd8-174">(There is also a **CComQIPtr** class, which is not discussed here.) Here is the [Open Dialog Box](example--the-open-dialog-box.md) example rewritten to use **CComPtr**.</span></span>


```C++
#include <windows.h>
#include <shobjidl.h> 
#include <atlbase.h> // Contains the declaration of CComPtr.

int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
        COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CComPtr<IFileOpenDialog> pFileOpen;

        // Create the FileOpenDialog object.
        hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
        if (SUCCEEDED(hr))
        {
            // Show the Open dialog box.
            hr = pFileOpen->Show(NULL);

            // Get the file name from the dialog box.
            if (SUCCEEDED(hr))
            {
                CComPtr<IShellItem> pItem;
                hr = pFileOpen->GetResult(&pItem);
                if (SUCCEEDED(hr))
                {
                    PWSTR pszFilePath;
                    hr = pItem->GetDisplayName(SIGDN_FILESYSPATH, &pszFilePath);

                    // Display the file name to the user.
                    if (SUCCEEDED(hr))
                    {
                        MessageBox(NULL, pszFilePath, L"File Path", MB_OK);
                        CoTaskMemFree(pszFilePath);
                    }
                }

                // pItem goes out of scope.
            }

            // pFileOpen goes out of scope.
        }
        CoUninitialize();
    }
    return 0;
}
```



<span data-ttu-id="33fd8-175">Основное различие между этим кодом и исходным примером состоит в том, что эта версия не вызывает явно [**выпуск**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="33fd8-175">The main difference between this code and the original example is that this version does not explicitly call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release).</span></span> <span data-ttu-id="33fd8-176">Когда экземпляр **CComPtr** выходит за пределы области действия, деструктор вызывает метод **Release** в базовом указателе.</span><span class="sxs-lookup"><span data-stu-id="33fd8-176">When the **CComPtr** instance goes out of scope, the destructor calls **Release** on the underlying pointer.</span></span>

<span data-ttu-id="33fd8-177">**CComPtr** — это шаблон класса.</span><span class="sxs-lookup"><span data-stu-id="33fd8-177">**CComPtr** is a class template.</span></span> <span data-ttu-id="33fd8-178">Аргумент шаблона является типом COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="33fd8-178">The template argument is the COM interface type.</span></span> <span data-ttu-id="33fd8-179">Внутри **CComPtr** содержит указатель этого типа.</span><span class="sxs-lookup"><span data-stu-id="33fd8-179">Internally, **CComPtr** holds a pointer of that type.</span></span> <span data-ttu-id="33fd8-180">**CComPtr** переопределяет **оператор-> ()** и **оператор& ()** , чтобы класс действовал как базовый указатель.</span><span class="sxs-lookup"><span data-stu-id="33fd8-180">**CComPtr** overrides **operator->()** and **operator&()** so that the class acts like the underlying pointer.</span></span> <span data-ttu-id="33fd8-181">Например, следующий код эквивалентен вызову метода **ифилеопендиалог::** reby напрямую:</span><span class="sxs-lookup"><span data-stu-id="33fd8-181">For example, the following code is equivalent to calling the **IFileOpenDialog::Show** method directly:</span></span>


```C++
hr = pFileOpen->Show(NULL);
```



<span data-ttu-id="33fd8-182">**CComPtr** также определяет метод **CComPtr:: CoCreateInstance** , который вызывает функцию COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с некоторыми значениями параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="33fd8-182">**CComPtr** also defines a **CComPtr::CoCreateInstance** method, which calls the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function with some default parameter values.</span></span> <span data-ttu-id="33fd8-183">Единственным обязательным параметром является идентификатор класса, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="33fd8-183">The only required parameter is the class identifier, as the next example shows:</span></span>


```C++
hr = pFileOpen.CoCreateInstance(__uuidof(FileOpenDialog));
```



<span data-ttu-id="33fd8-184">Метод **CComPtr:: CoCreateInstance** предоставляется исключительно в качестве удобства; При желании можно по-прежнему вызывать функцию COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="33fd8-184">The **CComPtr::CoCreateInstance** method is provided purely as a convenience; you can still call the COM [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, if you prefer.</span></span>

## <a name="next"></a><span data-ttu-id="33fd8-185">Следующая</span><span class="sxs-lookup"><span data-stu-id="33fd8-185">Next</span></span>

[<span data-ttu-id="33fd8-186">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="33fd8-186">Error Handling in COM</span></span>](error-handling-in-com.md)

 

 