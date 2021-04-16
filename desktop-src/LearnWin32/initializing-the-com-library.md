---
title: Инициализация библиотеки COM
description: Инициализация библиотеки COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105672284"
---
# <a name="initializing-the-com-library"></a><span data-ttu-id="ea74a-103">Инициализация библиотеки COM</span><span class="sxs-lookup"><span data-stu-id="ea74a-103">Initializing the COM Library</span></span>

<span data-ttu-id="ea74a-104">Любая программа Windows, использующая COM, должна инициализировать библиотеку COM, вызвав функцию [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) .</span><span class="sxs-lookup"><span data-stu-id="ea74a-104">Any Windows program that uses COM must initialize the COM library by calling the [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) function.</span></span> <span data-ttu-id="ea74a-105">Каждый поток, использующий интерфейс COM, должен выполнять отдельный вызов этой функции.</span><span class="sxs-lookup"><span data-stu-id="ea74a-105">Each thread that uses a COM interface must make a separate call to this function.</span></span> <span data-ttu-id="ea74a-106">**CoInitializeEx** имеет следующую сигнатуру:</span><span class="sxs-lookup"><span data-stu-id="ea74a-106">**CoInitializeEx** has the following signature:</span></span>


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



<span data-ttu-id="ea74a-107">Первый параметр зарезервирован и должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ea74a-107">The first parameter is reserved and must be **NULL**.</span></span> <span data-ttu-id="ea74a-108">Второй параметр указывает потоковую модель, которую будет использовать программа.</span><span class="sxs-lookup"><span data-stu-id="ea74a-108">The second parameter specifies the threading model that your program will use.</span></span> <span data-ttu-id="ea74a-109">Модель COM поддерживает две различные модели потоков, потоковое *и* *многопоточное* .</span><span class="sxs-lookup"><span data-stu-id="ea74a-109">COM supports two different threading models, *apartment threaded* and *multithreaded*.</span></span> <span data-ttu-id="ea74a-110">При указании потоков подразделений выполняются следующие гарантии.</span><span class="sxs-lookup"><span data-stu-id="ea74a-110">If you specify apartment threading, you are making the following guarantees:</span></span>

-   <span data-ttu-id="ea74a-111">Вы будете обращаться к каждому COM-объекту из одного потока; указатели на COM-интерфейсы не будут совместно использоваться несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="ea74a-111">You will access each COM object from a single thread; you will not share COM interface pointers between multiple threads.</span></span>
-   <span data-ttu-id="ea74a-112">Поток будет иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="ea74a-112">The thread will have a message loop.</span></span> <span data-ttu-id="ea74a-113">(См. [окно сообщения](window-messages.md) в модуле 1.)</span><span class="sxs-lookup"><span data-stu-id="ea74a-113">(See [Window Messages](window-messages.md) in Module 1.)</span></span>

<span data-ttu-id="ea74a-114">Если какое-либо из этих ограничений не равно true, используйте многопоточность модели.</span><span class="sxs-lookup"><span data-stu-id="ea74a-114">If either of these constraints is not true, use the multithreaded model.</span></span> <span data-ttu-id="ea74a-115">Чтобы указать потоковую модель, установите один из следующих флагов в параметре *двкоинит* .</span><span class="sxs-lookup"><span data-stu-id="ea74a-115">To specify the threading model, set one of the following flags in the *dwCoInit* parameter.</span></span>



| <span data-ttu-id="ea74a-116">Flag</span><span class="sxs-lookup"><span data-stu-id="ea74a-116">Flag</span></span>                          | <span data-ttu-id="ea74a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ea74a-117">Description</span></span>         |
|-------------------------------|---------------------|
| <span data-ttu-id="ea74a-118">**\_апартментсреадед**</span><span class="sxs-lookup"><span data-stu-id="ea74a-118">**COINIT\_APARTMENTTHREADED**</span></span> | <span data-ttu-id="ea74a-119">Потоковое подразделение.</span><span class="sxs-lookup"><span data-stu-id="ea74a-119">Apartment threaded.</span></span> |
| <span data-ttu-id="ea74a-120">**Многопотоковая ИНИЦИАЛИЗАЦИя \_**</span><span class="sxs-lookup"><span data-stu-id="ea74a-120">**COINIT\_MULTITHREADED**</span></span>     | <span data-ttu-id="ea74a-121">Многопоточных.</span><span class="sxs-lookup"><span data-stu-id="ea74a-121">Multithreaded.</span></span>      |



 

<span data-ttu-id="ea74a-122">Необходимо задать только один из этих флагов.</span><span class="sxs-lookup"><span data-stu-id="ea74a-122">You must set exactly one of these flags.</span></span> <span data-ttu-id="ea74a-123">Как правило, поток, создающий окно, должен использовать флаг **коinit \_ апартментсреадед** , а другие потоки должны использовать **\_ многопотоковую инициализацию**.</span><span class="sxs-lookup"><span data-stu-id="ea74a-123">Generally, a thread that creates a window should use the **COINIT\_APARTMENTTHREADED** flag, and other threads should use **COINIT\_MULTITHREADED**.</span></span> <span data-ttu-id="ea74a-124">Однако для некоторых COM-компонентов требуется конкретная потоковая модель.</span><span class="sxs-lookup"><span data-stu-id="ea74a-124">However, some COM components require a particular threading model.</span></span> <span data-ttu-id="ea74a-125">В документации MSDN следует сообщить, когда это так.</span><span class="sxs-lookup"><span data-stu-id="ea74a-125">The MSDN documentation should tell you when that is the case.</span></span>

> [!Note]  
> <span data-ttu-id="ea74a-126">На самом деле, даже при указании потоков подразделений все равно можно совместно использовать интерфейсы между потоками, используя метод, именуемый *упаковкой*.</span><span class="sxs-lookup"><span data-stu-id="ea74a-126">Actually, even if you specify apartment threading, it is still possible to share interfaces between threads, by using a technique called *marshaling*.</span></span> <span data-ttu-id="ea74a-127">Упаковка выходит за рамки этого модуля.</span><span class="sxs-lookup"><span data-stu-id="ea74a-127">Marshaling is beyond the scope of this module.</span></span> <span data-ttu-id="ea74a-128">Важно отметить, что при работе с потоковыми апартаментами никогда не нужно просто копировать указатель интерфейса в другой поток.</span><span class="sxs-lookup"><span data-stu-id="ea74a-128">The important point is that with apartment threading, you must never simply copy an interface pointer to another thread.</span></span> <span data-ttu-id="ea74a-129">Дополнительные сведения о потоковых моделях COM см. в разделе [процессы, потоки и подразделения](/windows/desktop/com/processes--threads--and-apartments).</span><span class="sxs-lookup"><span data-stu-id="ea74a-129">For more information about the COM threading models, see [Processes, Threads, and Apartments](/windows/desktop/com/processes--threads--and-apartments).</span></span>

 

<span data-ttu-id="ea74a-130">В дополнение к уже упомянутым флагам рекомендуется установить флаг **\_ \_ OLE1DDE Disabled** в параметре *двкоинит* .</span><span class="sxs-lookup"><span data-stu-id="ea74a-130">In addition to the flags already mentioned, it is a good idea to set the **COINIT\_DISABLE\_OLE1DDE** flag in the *dwCoInit* parameter.</span></span> <span data-ttu-id="ea74a-131">Установка этого флага позволяет избежать некоторых издержек, связанных с связыванием и внедрением объектов (OLE) 1,0, устаревшей технологией.</span><span class="sxs-lookup"><span data-stu-id="ea74a-131">Setting this flag avoids some overhead associated with Object Linking and Embedding (OLE) 1.0, an obsolete technology.</span></span>

<span data-ttu-id="ea74a-132">Вот как можно инициализировать COM для потоков подразделений:</span><span class="sxs-lookup"><span data-stu-id="ea74a-132">Here is how you would initialize COM for apartment threading:</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



<span data-ttu-id="ea74a-133">Возвращаемый тип **HRESULT** содержит код ошибки или успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ea74a-133">The **HRESULT** return type contains an error or success code.</span></span> <span data-ttu-id="ea74a-134">В следующем разделе мы рассмотрим обработку ошибок COM.</span><span class="sxs-lookup"><span data-stu-id="ea74a-134">We'll look at COM error handling in the next section.</span></span>

## <a name="uninitializing-the-com-library"></a><span data-ttu-id="ea74a-135">Отмена инициализации библиотеки COM</span><span class="sxs-lookup"><span data-stu-id="ea74a-135">Uninitializing the COM Library</span></span>

<span data-ttu-id="ea74a-136">Для каждого успешного вызова [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)необходимо вызвать [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) перед выходом из потока.</span><span class="sxs-lookup"><span data-stu-id="ea74a-136">For every successful call to [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), you must call [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) before the thread exits.</span></span> <span data-ttu-id="ea74a-137">Эта функция не принимает параметров и не имеет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ea74a-137">This function takes no parameters and has no return value.</span></span>


```C++
CoUninitialize();
```



## <a name="next"></a><span data-ttu-id="ea74a-138">Следующая</span><span class="sxs-lookup"><span data-stu-id="ea74a-138">Next</span></span>

[<span data-ttu-id="ea74a-139">Коды ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="ea74a-139">Error Codes in COM</span></span>](error-codes-in-com.md)

 

 