---
title: Создание объекта в COM
description: Чтобы использовать COM-интерфейс, программа сначала создает экземпляр объекта, который реализует этот интерфейс.
ms.assetid: 75f2115d-d49d-4e4e-8f99-67a231559ba6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f96e4d9c2afbac028bfcefffcec6a070c78c8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412872"
---
# <a name="creating-an-object-in-com"></a><span data-ttu-id="42756-103">Создание объекта в COM</span><span class="sxs-lookup"><span data-stu-id="42756-103">Creating an Object in COM</span></span>

<span data-ttu-id="42756-104">После того как поток инициализирует библиотеку COM, поток может использовать COM-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="42756-104">After a thread has initialized the COM library, it is safe for the thread to use COM interfaces.</span></span> <span data-ttu-id="42756-105">Чтобы использовать COM-интерфейс, программа сначала создает экземпляр объекта, который реализует этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="42756-105">To use a COM interface, your program first creates an instance of an object that implements that interface.</span></span>

<span data-ttu-id="42756-106">Как правило, существует два способа создания COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="42756-106">In general, there are two ways to create a COM object:</span></span>

-   <span data-ttu-id="42756-107">Модуль, реализующий объект, может предоставить функцию, специально предназначенную для создания экземпляров этого объекта.</span><span class="sxs-lookup"><span data-stu-id="42756-107">The module that implements the object might provide a function specifically designed to create instances of that object.</span></span>
-   <span data-ttu-id="42756-108">Кроме того, COM предоставляет универсальную функцию создания с именем [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="42756-108">Alternatively, COM provides a generic creation function named [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="42756-109">Например, возьмем гипотетический `Shape` объект из раздела [что такое COM-интерфейс?](what-is-a-com-interface-.md).</span><span class="sxs-lookup"><span data-stu-id="42756-109">For example, take the hypothetical `Shape` object from the topic [What Is a COM Interface?](what-is-a-com-interface-.md).</span></span> <span data-ttu-id="42756-110">В этом примере `Shape` объект реализует интерфейс с именем `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="42756-110">In that example, the `Shape` object implements an interface named `IDrawable`.</span></span> <span data-ttu-id="42756-111">Библиотека графики, реализующая `Shape` объект, может экспортировать функцию со следующей сигнатурой.</span><span class="sxs-lookup"><span data-stu-id="42756-111">The graphics library that implements the `Shape` object might export a function with the following signature.</span></span>


```C++
// Not an actual Windows function. 

HRESULT CreateShape(IDrawable** ppShape);
```



<span data-ttu-id="42756-112">Используя эту функцию, можно создать новый объект, `Shape` как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="42756-112">Given this function, you could create a new `Shape` object as follows.</span></span>


```C++
IDrawable *pShape;

HRESULT hr = CreateShape(&pShape);
if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="42756-113">Параметр *ппшапе* имеет тип указателя на указатель на `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="42756-113">The *ppShape* parameter is of type pointer-to-pointer-to-`IDrawable`.</span></span> <span data-ttu-id="42756-114">Если вы ранее не видели этот шаблон, двойное косвенное обращение может быть замешательство.</span><span class="sxs-lookup"><span data-stu-id="42756-114">If you have not seen this pattern before, the double indirection might be puzzling.</span></span>

<span data-ttu-id="42756-115">Рассмотрим требования `CreateShape` функции.</span><span class="sxs-lookup"><span data-stu-id="42756-115">Consider the requirements of the `CreateShape` function.</span></span> <span data-ttu-id="42756-116">Функция должна предоставить `IDrawable` указатель обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="42756-116">The function must give an `IDrawable` pointer back to the caller.</span></span> <span data-ttu-id="42756-117">Но возвращаемое значение функции уже используется для кода ошибки или успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="42756-117">But the function's return value is already used for the error/success code.</span></span> <span data-ttu-id="42756-118">Поэтому указатель должен возвращаться к функции с помощью аргумента.</span><span class="sxs-lookup"><span data-stu-id="42756-118">Therefore, the pointer must be returned through an argument to the function.</span></span> <span data-ttu-id="42756-119">Вызывающий объект передаст в функцию переменную типа `IDrawable*` , и эта переменная будет перезаписана новым `IDrawable` указателем.</span><span class="sxs-lookup"><span data-stu-id="42756-119">The caller will pass a variable of type `IDrawable*` to the function, and the function will overwrite this variable with a new `IDrawable` pointer.</span></span> <span data-ttu-id="42756-120">В C++ существует два способа перезаписи значения параметра функцией: передать по ссылке или передать по адресу.</span><span class="sxs-lookup"><span data-stu-id="42756-120">In C++, there are only two ways for a function to overwrite a parameter value: pass by reference, or pass by address.</span></span> <span data-ttu-id="42756-121">В COM используется последняя передача по адресу.</span><span class="sxs-lookup"><span data-stu-id="42756-121">COM uses the latter, pass-by-address.</span></span> <span data-ttu-id="42756-122">И адрес указателя является указателем на указатель, поэтому тип параметра должен быть `IDrawable**` .</span><span class="sxs-lookup"><span data-stu-id="42756-122">And the address of a pointer is a pointer-to-a-pointer, so the parameter type must be `IDrawable**`.</span></span>

<span data-ttu-id="42756-123">Ниже приведена схема, помогающая визуализировать то, что происходит.</span><span class="sxs-lookup"><span data-stu-id="42756-123">Here is a diagram to help visualize what's going on.</span></span>

![Схема, показывающая косвенное обращение между указателями](images/com03.png)

<span data-ttu-id="42756-125">`CreateShape`Функция использует адрес *пшапе* ( `&pShape` ) для записи нового значения указателя в *пшапе*.</span><span class="sxs-lookup"><span data-stu-id="42756-125">The `CreateShape` function uses the address of *pShape* (`&pShape`) to write a new pointer value to *pShape*.</span></span>

## <a name="cocreateinstance-a-generic-way-to-create-objects"></a><span data-ttu-id="42756-126">CoCreateInstance — универсальный способ создания объектов</span><span class="sxs-lookup"><span data-stu-id="42756-126">CoCreateInstance: A Generic Way to Create Objects</span></span>

<span data-ttu-id="42756-127">Функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) предоставляет универсальный механизм для создания объектов.</span><span class="sxs-lookup"><span data-stu-id="42756-127">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function provides a generic mechanism for creating objects.</span></span> <span data-ttu-id="42756-128">Для понимания **CoCreateInstance** необходимо помнить, что два COM-объекта могут реализовывать один и тот же интерфейс, и один объект может реализовать два или больше интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="42756-128">To understand **CoCreateInstance**, keep in mind that two COM objects can implement the same interface, and one object can implement two or more interfaces.</span></span> <span data-ttu-id="42756-129">Таким словами, универсальной функции, создающей объекты, требуется два фрагмента информации.</span><span class="sxs-lookup"><span data-stu-id="42756-129">Thus, a generic function that creates objects needs two pieces of information.</span></span>

-   <span data-ttu-id="42756-130">Создаваемый объект.</span><span class="sxs-lookup"><span data-stu-id="42756-130">Which object to create.</span></span>
-   <span data-ttu-id="42756-131">Интерфейс, который необходимо получить из объекта.</span><span class="sxs-lookup"><span data-stu-id="42756-131">Which interface to get from the object.</span></span>

<span data-ttu-id="42756-132">Но как указать эту информацию при вызове функции?</span><span class="sxs-lookup"><span data-stu-id="42756-132">But how do we indicate this information when we call the function?</span></span> <span data-ttu-id="42756-133">В COM объект или интерфейс определяется путем присвоения ему 128-разрядного числа, называемого *глобально уникальным идентификатором* (GUID).</span><span class="sxs-lookup"><span data-stu-id="42756-133">In COM, an object or an interface is identified by assigning it a 128-bit number, called a *globally unique identifier* (GUID).</span></span> <span data-ttu-id="42756-134">Идентификаторы GUID создаются таким образом, что они эффективно уникальны.</span><span class="sxs-lookup"><span data-stu-id="42756-134">GUIDs are generated in a way that makes them effectively unique.</span></span> <span data-ttu-id="42756-135">Идентификаторы GUID — это решение проблемы создания уникальных идентификаторов без центрального центра регистрации.</span><span class="sxs-lookup"><span data-stu-id="42756-135">GUIDs are a solution to the problem of how to create unique identifiers without a central registration authority.</span></span> <span data-ttu-id="42756-136">Идентификаторы GUID иногда называются *универсальными уникальными идентификаторами* (UUID).</span><span class="sxs-lookup"><span data-stu-id="42756-136">GUIDs are sometimes called *universally unique identifiers* (UUIDs).</span></span> <span data-ttu-id="42756-137">До COM они использовались в DCE/RPC (распределенные вычислительные среды или удаленный вызов процедур).</span><span class="sxs-lookup"><span data-stu-id="42756-137">Prior to COM, they were used in DCE/RPC (Distributed Computing Environment/Remote Procedure Call).</span></span> <span data-ttu-id="42756-138">Для создания новых идентификаторов GUID существует несколько алгоритмов.</span><span class="sxs-lookup"><span data-stu-id="42756-138">Several algorithms exist for creating new GUIDs.</span></span> <span data-ttu-id="42756-139">Не все эти алгоритмы строго гарантируют уникальность, но вероятность случайного создания одного и того же значения GUID в два раза очень мала — фактически ноль.</span><span class="sxs-lookup"><span data-stu-id="42756-139">Not all of these algorithms strictly guarantee uniqueness, but the probability of accidentally creating the same GUID value twice is extremely small—effectively zero.</span></span> <span data-ttu-id="42756-140">Идентификаторы GUID можно использовать для обнаружения любой сущности, а не только для объектов и интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="42756-140">GUIDs can be used to identify any sort of entity, not just objects and interfaces.</span></span> <span data-ttu-id="42756-141">Тем не менее, это единственное использование, которое касается нас в этом модуле.</span><span class="sxs-lookup"><span data-stu-id="42756-141">However, that is the only use that concerns us in this module.</span></span>

<span data-ttu-id="42756-142">Например, `Shapes` Библиотека может объявлять две константы GUID:</span><span class="sxs-lookup"><span data-stu-id="42756-142">For example, the `Shapes` library might declare two GUID constants:</span></span>


```C++
extern const GUID CLSID_Shape;
extern const GUID IID_IDrawable; 
```



<span data-ttu-id="42756-143">(Можно предположить, что фактические 128-разрядные числовые значения для этих констант определены в других местах.) **\_ Фигура** константы CLSID определяет `Shape` объект, а константа **IID \_ идравабле** определяет `IDrawable` интерфейс.</span><span class="sxs-lookup"><span data-stu-id="42756-143">(You can assume that the actual 128-bit numeric values for these constants are defined elsewhere.) The constant **CLSID\_Shape** identifies the `Shape` object, while the constant **IID\_IDrawable** identifies the `IDrawable` interface.</span></span> <span data-ttu-id="42756-144">Префикс "CLSID" означает *идентификатор класса*, а префикс *IID* означает *идентификатор интерфейса*.</span><span class="sxs-lookup"><span data-stu-id="42756-144">The prefix "CLSID" stands for *class identifier*, and the prefix *IID* stands for *interface identifier*.</span></span> <span data-ttu-id="42756-145">Это стандартные соглашения об именовании в COM.</span><span class="sxs-lookup"><span data-stu-id="42756-145">These are standard naming conventions in COM.</span></span>

<span data-ttu-id="42756-146">Учитывая эти значения, вы создадите новый `Shape` экземпляр следующим образом:</span><span class="sxs-lookup"><span data-stu-id="42756-146">Given these values, you would create a new `Shape` instance as follows:</span></span>


```C++
IDrawable *pShape;
hr = CoCreateInstance(CLSID_Shape, NULL, CLSCTX_INPROC_SERVER, IID_Drawable,
     reinterpret_cast<void**>(&pShape));

if (SUCCEEDED(hr))
{
    // Use the Shape object.
}
else
{
    // An error occurred.
}
```



<span data-ttu-id="42756-147">Функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) имеет пять параметров.</span><span class="sxs-lookup"><span data-stu-id="42756-147">The [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function has five parameters.</span></span> <span data-ttu-id="42756-148">Первый и четвертый параметры являются идентификатором класса и идентификатором интерфейса.</span><span class="sxs-lookup"><span data-stu-id="42756-148">The first and fourth parameters are the class identifier and interface identifier.</span></span> <span data-ttu-id="42756-149">Фактически эти параметры указывают функции "создать объект Shape" и присвоить мне указатель на интерфейс Идравабле ".</span><span class="sxs-lookup"><span data-stu-id="42756-149">In effect, these parameters tell the function, "Create the Shape object, and give me a pointer to the IDrawable interface."</span></span>

<span data-ttu-id="42756-150">Установите для второго параметра **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="42756-150">Set the second parameter to **NULL**.</span></span> <span data-ttu-id="42756-151">(Дополнительные сведения о значении этого параметра см. в разделе [агрегирование](/windows/desktop/com/aggregation) разделов в документации по com.) Третий параметр принимает набор флагов, основной целью которых является указание *контекста выполнения* для объекта.</span><span class="sxs-lookup"><span data-stu-id="42756-151">(For more information about the meaning of this parameter, see the topic [Aggregation](/windows/desktop/com/aggregation) in the COM documentation.) The third parameter takes a set of flags whose main purpose is to specify the *execution context* for the object.</span></span> <span data-ttu-id="42756-152">Контекст выполнения определяет, выполняется ли объект в том же процессе, что и приложение. в другом процессе на том же компьютере; или на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="42756-152">The execution context specifies whether the object runs in the same process as the application; in a different process on the same computer; or on a remote computer.</span></span> <span data-ttu-id="42756-153">В следующей таблице показаны наиболее распространенные значения для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="42756-153">The following table shows the most common values for this parameter.</span></span>



| <span data-ttu-id="42756-154">Flag</span><span class="sxs-lookup"><span data-stu-id="42756-154">Flag</span></span>                       | <span data-ttu-id="42756-155">Описание</span><span class="sxs-lookup"><span data-stu-id="42756-155">Description</span></span>                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42756-156">**КЛСКТКС \_ INPROC \_ Server**</span><span class="sxs-lookup"><span data-stu-id="42756-156">**CLSCTX\_INPROC\_SERVER**</span></span> | <span data-ttu-id="42756-157">Тот же процесс.</span><span class="sxs-lookup"><span data-stu-id="42756-157">Same process.</span></span>                                                                                                                                                      |
| <span data-ttu-id="42756-158">**\_локальный \_ сервер клскткс**</span><span class="sxs-lookup"><span data-stu-id="42756-158">**CLSCTX\_LOCAL\_SERVER**</span></span>  | <span data-ttu-id="42756-159">Другой процесс, один и тот же компьютер.</span><span class="sxs-lookup"><span data-stu-id="42756-159">Different process, same computer.</span></span>                                                                                                                                  |
| <span data-ttu-id="42756-160">**\_Удаленный \_ сервер клскткс**</span><span class="sxs-lookup"><span data-stu-id="42756-160">**CLSCTX\_REMOTE\_SERVER**</span></span> | <span data-ttu-id="42756-161">Другой компьютер.</span><span class="sxs-lookup"><span data-stu-id="42756-161">Different computer.</span></span>                                                                                                                                                |
| <span data-ttu-id="42756-162">**КЛСКТКС \_ все**</span><span class="sxs-lookup"><span data-stu-id="42756-162">**CLSCTX\_ALL**</span></span>            | <span data-ttu-id="42756-163">Используйте наиболее эффективный вариант, который поддерживает объект.</span><span class="sxs-lookup"><span data-stu-id="42756-163">Use the most efficient option that the object supports.</span></span> <span data-ttu-id="42756-164">(Ранжирование, от наиболее эффективного до наименее эффективного, — это внутрипроцессный, внутрипроцессный и перекрестный компьютер.)</span><span class="sxs-lookup"><span data-stu-id="42756-164">(The ranking, from most efficient to least efficient, is: in-process, out-of-process, and cross-computer.)</span></span> |



 

<span data-ttu-id="42756-165">Документация по конкретному компоненту может сообщить, какой контекст выполнения поддерживает объект.</span><span class="sxs-lookup"><span data-stu-id="42756-165">The documentation for a particular component might tell you which execution context the object supports.</span></span> <span data-ttu-id="42756-166">В противном случае используйте **клскткс \_ ALL**.</span><span class="sxs-lookup"><span data-stu-id="42756-166">If not, use **CLSCTX\_ALL**.</span></span> <span data-ttu-id="42756-167">Если вы запрашиваете контекст выполнения, который не поддерживает объект, функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) возвращает код ошибки **регдб \_ E \_ класснотрег**.</span><span class="sxs-lookup"><span data-stu-id="42756-167">If you request an execution context that the object does not support, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function returns the error code **REGDB\_E\_CLASSNOTREG**.</span></span> <span data-ttu-id="42756-168">Этот код ошибки также может указывать на то, что CLSID не соответствует ни одному компоненту, зарегистрированному на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="42756-168">This error code can also indicate that the CLSID does not correspond to any component registered on the user's computer.</span></span>

<span data-ttu-id="42756-169">Пятый параметр для [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) получает указатель на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="42756-169">The fifth parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) receives a pointer to the interface.</span></span> <span data-ttu-id="42756-170">Поскольку **CoCreateInstance** является универсальным механизмом, этот параметр не может быть строго типизированным.</span><span class="sxs-lookup"><span data-stu-id="42756-170">Because **CoCreateInstance** is a generic mechanism, this parameter cannot be strongly typed.</span></span> <span data-ttu-id="42756-171">Вместо этого тип данных — **void \* \***, и вызывающий объект должен привести адрес указателя к типу **void \* \*** .</span><span class="sxs-lookup"><span data-stu-id="42756-171">Instead, the data type is **void\*\***, and the caller must coerce the address of the pointer to a **void\*\*** type.</span></span> <span data-ttu-id="42756-172">Это предназначение **переинтерпретации \_** в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="42756-172">That is the purpose of the **reinterpret\_cast** in the previous example.</span></span>

<span data-ttu-id="42756-173">Важно проверить возвращаемое значение [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="42756-173">It is crucial to check the return value of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="42756-174">Если функция возвращает код ошибки, указатель интерфейса COM является недопустимым, и попытка его разыменования может привести к сбою программы.</span><span class="sxs-lookup"><span data-stu-id="42756-174">If the function returns an error code, the COM interface pointer is invalid, and attempting to dereference it can cause your program to crash.</span></span>

<span data-ttu-id="42756-175">Внутри функция [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) использует различные методы для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="42756-175">Internally, the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function uses various techniques to create an object.</span></span> <span data-ttu-id="42756-176">В самом простом случае он ищет идентификатор класса в реестре.</span><span class="sxs-lookup"><span data-stu-id="42756-176">In the simplest case, it looks up the class identifier in the registry.</span></span> <span data-ttu-id="42756-177">Запись реестра указывает на DLL или EXE-файл, который реализует объект.</span><span class="sxs-lookup"><span data-stu-id="42756-177">The registry entry points to a DLL or EXE that implements the object.</span></span> <span data-ttu-id="42756-178">**CoCreateInstance** также может использовать сведения из каталога COM+ или параллельного манифеста (SxS).</span><span class="sxs-lookup"><span data-stu-id="42756-178">**CoCreateInstance** can also use information from a COM+ catalog or a side-by-side (SxS) manifest.</span></span> <span data-ttu-id="42756-179">Независимо от того, что сведения прозрачны для вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="42756-179">Regardless, the details are transparent to the caller.</span></span> <span data-ttu-id="42756-180">Дополнительные сведения о внутренних деталях **CoCreateInstance** см. в разделе [COM-клиенты и серверы](/windows/desktop/com/com-clients-and-servers).</span><span class="sxs-lookup"><span data-stu-id="42756-180">For more information about the internal details of **CoCreateInstance**, see [COM Clients and Servers](/windows/desktop/com/com-clients-and-servers).</span></span>

<span data-ttu-id="42756-181">`Shapes`Пример, который мы использовали, немного надуманный, так что теперь давайте вернемся к реальному примеру com в действии: Отображение диалогового окна **Открыть** для пользователя, чтобы выбрать файл.</span><span class="sxs-lookup"><span data-stu-id="42756-181">The `Shapes` example that we have been using is somewhat contrived, so now let's turn to a real-world example of COM in action: displaying the **Open** dialog box for the user to select a file.</span></span>

## <a name="next"></a><span data-ttu-id="42756-182">Следующая</span><span class="sxs-lookup"><span data-stu-id="42756-182">Next</span></span>

[<span data-ttu-id="42756-183">Пример. диалоговое окно "Открыть"</span><span class="sxs-lookup"><span data-stu-id="42756-183">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)

 

 