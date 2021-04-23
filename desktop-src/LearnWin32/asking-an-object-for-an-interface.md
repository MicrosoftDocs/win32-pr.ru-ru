---
title: Запрос объекта для интерфейса
description: Запрос объекта для интерфейса
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070013"
---
# <a name="asking-an-object-for-an-interface"></a><span data-ttu-id="5f848-103">Запрос объекта для интерфейса</span><span class="sxs-lookup"><span data-stu-id="5f848-103">Asking an Object for an Interface</span></span>

<span data-ttu-id="5f848-104">Ранее мы видели, что объект может реализовать более одного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5f848-104">We saw earlier that an object can implement more than one interface.</span></span> <span data-ttu-id="5f848-105">Объект диалогового окна общих элементов является реальным примером этого.</span><span class="sxs-lookup"><span data-stu-id="5f848-105">The Common Item Dialog object is a real-world example of this.</span></span> <span data-ttu-id="5f848-106">Для поддержки наиболее типичных применений объект реализует интерфейс [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="5f848-106">To support the most typical uses, the object implements the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span> <span data-ttu-id="5f848-107">Этот интерфейс определяет основные методы для отображения диалогового окна и получения сведений о выбранном файле.</span><span class="sxs-lookup"><span data-stu-id="5f848-107">This interface defines basic methods for displaying the dialog box and getting information about the selected file.</span></span> <span data-ttu-id="5f848-108">Однако для более сложного использования объект также реализует интерфейс с именем [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize).</span><span class="sxs-lookup"><span data-stu-id="5f848-108">For more advanced use, however, the object also implements an interface named [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize).</span></span> <span data-ttu-id="5f848-109">Программа может использовать этот интерфейс для настройки внешнего вида и поведения диалогового окна путем добавления новых элементов управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5f848-109">A program can use this interface to customize the appearance and behavior of the dialog box, by adding new UI controls.</span></span>

<span data-ttu-id="5f848-110">Вспомним, что каждый COM-интерфейс должен прямо или косвенно наследовать от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5f848-110">Recall that every COM interface must inherit, directly or indirectly, from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5f848-111">На следующей схеме показано наследование объекта диалогового окна общих элементов.</span><span class="sxs-lookup"><span data-stu-id="5f848-111">The following diagram shows the inheritance of the Common Item Dialog object.</span></span>

![Схема, показывающая интерфейсы, предоставляемые объектом диалогового окна общих элементов](images/com06.png)

<span data-ttu-id="5f848-113">Как видно из схемы, прямым предком [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) является интерфейс [**ифиледиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , который, в свою очередь, наследует [**имодалвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="5f848-113">As you can see from the diagram, the direct ancestor of [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) is the [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) interface, which in turn inherits [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="5f848-114">Когда вы переходите к цепочке наследования от **ифилеопендиалог** к **имодалвиндов**, интерфейсы определяют все более обобщенные функциональные возможности окна.</span><span class="sxs-lookup"><span data-stu-id="5f848-114">As you go up the inheritance chain from **IFileOpenDialog** to **IModalWindow**, the interfaces define increasingly generalized window functionality.</span></span> <span data-ttu-id="5f848-115">Наконец, интерфейс **имодалвиндов** наследует [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="5f848-115">Finally, the **IModalWindow** interface inherits [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="5f848-116">Объект диалогового окна общего элемента также реализует [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), который существует в отдельной цепочке наследования.</span><span class="sxs-lookup"><span data-stu-id="5f848-116">The Common Item Dialog object also implements [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), which exists in a separate inheritance chain.</span></span>

<span data-ttu-id="5f848-117">Теперь предположим, что у вас есть указатель на интерфейс [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) .</span><span class="sxs-lookup"><span data-stu-id="5f848-117">Now suppose that you have a pointer to the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) interface.</span></span> <span data-ttu-id="5f848-118">Как можно получить указатель на интерфейс [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?</span><span class="sxs-lookup"><span data-stu-id="5f848-118">How would you get a pointer to the [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) interface?</span></span>

![Схема, в которой показаны два указателя интерфейса на интерфейсы в одном объекте](images/com07.png)

<span data-ttu-id="5f848-120">Простое приведение указателя [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) к указателю [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) не будет работать.</span><span class="sxs-lookup"><span data-stu-id="5f848-120">Simply casting the [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) pointer to an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer will not work.</span></span> <span data-ttu-id="5f848-121">В иерархии наследования нет надежного способа «перекрестное приведение» без какой-либо формы информации о типах во время выполнения (RTTI), что является очень зависимым от языка функцией.</span><span class="sxs-lookup"><span data-stu-id="5f848-121">There is no reliable way to "cross cast" across an inheritance hierarchy, without some form of run-time type information (RTTI), which is a highly language-dependent feature.</span></span>

<span data-ttu-id="5f848-122">Подход COM заключается *в том, чтобы предоставить* объекту указатель [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , используя первый интерфейс в качестве программы передачи в объект.</span><span class="sxs-lookup"><span data-stu-id="5f848-122">The COM approach is to *ask* the object to give you an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer, using the first interface as a conduit into the object.</span></span> <span data-ttu-id="5f848-123">Это делается путем вызова метода [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) из первого указателя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5f848-123">This is done by calling the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method from the first interface pointer.</span></span> <span data-ttu-id="5f848-124">**QueryInterface** можно считать независимым от языка версией ключевого слова **Dynamic \_ Cast** в C++.</span><span class="sxs-lookup"><span data-stu-id="5f848-124">You can think of **QueryInterface** as a language-independent version of the **dynamic\_cast** keyword in C++.</span></span>

<span data-ttu-id="5f848-125">Метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) имеет следующую сигнатуру:</span><span class="sxs-lookup"><span data-stu-id="5f848-125">The [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method has the following signature:</span></span>

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

<span data-ttu-id="5f848-126">В зависимости от того, что вы уже знаете о [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), вы можете угадать, как работает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="5f848-126">Based on what you already know about [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), you might be able to guess how [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) works.</span></span>

-   <span data-ttu-id="5f848-127">Параметр *riid* — это идентификатор GUID, определяющий интерфейс, который вы запрашиваете.</span><span class="sxs-lookup"><span data-stu-id="5f848-127">The *riid* parameter is the GUID that identifies the interface you are asking for.</span></span> <span data-ttu-id="5f848-128">Тип данных **рефиид** является **typedef** для `const GUID&` .</span><span class="sxs-lookup"><span data-stu-id="5f848-128">The data type **REFIID** is a **typedef** for `const GUID&`.</span></span> <span data-ttu-id="5f848-129">Обратите внимание, что идентификатор класса (CLSID) не является обязательным, поскольку объект уже был создан.</span><span class="sxs-lookup"><span data-stu-id="5f848-129">Notice that the class identifier (CLSID) is not required, because the object has already been created.</span></span> <span data-ttu-id="5f848-130">Требуется только идентификатор интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5f848-130">Only the interface identifier is necessary.</span></span>
-   <span data-ttu-id="5f848-131">Параметр *ппвобжект* получает указатель на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5f848-131">The *ppvObject* parameter receives a pointer to the interface.</span></span> <span data-ttu-id="5f848-132">Тип данных этого параметра — **\* \* void**, по той же причине, что [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) использует этот тип данных: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) может использоваться для запроса любого COM-интерфейса, поэтому параметр не может быть строго типизирован.</span><span class="sxs-lookup"><span data-stu-id="5f848-132">The data type of this parameter is **void\*\***, for the same reason that [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) uses this data type: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) can be used to query for any COM interface, so the parameter cannot be strongly typed.</span></span>

<span data-ttu-id="5f848-133">Вот как можно вызвать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения указателя [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :</span><span class="sxs-lookup"><span data-stu-id="5f848-133">Here is how you would call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer:</span></span>


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="5f848-134">Как всегда, проверьте возвращаемое значение **HRESULT** в случае сбоя метода.</span><span class="sxs-lookup"><span data-stu-id="5f848-134">As always, check the **HRESULT** return value, in case the method fails.</span></span> <span data-ttu-id="5f848-135">Если метод завершится с ошибкой, необходимо вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , когда вы завершите работу с указателем, как описано в разделе [Управление временем существования объекта](managing-the-lifetime-of-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="5f848-135">If the method succeeds, you must call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) when you are done using the pointer, as described in [Managing the Lifetime of an Object](managing-the-lifetime-of-an-object.md).</span></span>

## <a name="next"></a><span data-ttu-id="5f848-136">Следующая</span><span class="sxs-lookup"><span data-stu-id="5f848-136">Next</span></span>

[<span data-ttu-id="5f848-137">Выделение памяти в COM</span><span class="sxs-lookup"><span data-stu-id="5f848-137">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)

 

 