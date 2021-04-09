---
title: Уникальные указатели
description: В программах на языке C более одного указателя могут содержать адрес данных.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070040"
---
# <a name="unique-pointers"></a><span data-ttu-id="ae409-103">Уникальные указатели</span><span class="sxs-lookup"><span data-stu-id="ae409-103">Unique Pointers</span></span>

<span data-ttu-id="ae409-104">В программах на языке C более одного указателя могут содержать адрес данных.</span><span class="sxs-lookup"><span data-stu-id="ae409-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="ae409-105">Указатели говорят, чтобы создать [*псевдоним*](a-glos.md) для данных.</span><span class="sxs-lookup"><span data-stu-id="ae409-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="ae409-106">Псевдонимы также создаются при наведении указателя на объявленные переменные.</span><span class="sxs-lookup"><span data-stu-id="ae409-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="ae409-107">В следующем фрагменте кода показаны оба метода присвоения псевдонимам.</span><span class="sxs-lookup"><span data-stu-id="ae409-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="ae409-108">В обычной программе на языке C можно указать двоичное дерево, используя следующее определение:</span><span class="sxs-lookup"><span data-stu-id="ae409-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="ae409-109">Доступ к содержимому узла дерева может осуществляться более чем одним указателем.</span><span class="sxs-lookup"><span data-stu-id="ae409-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="ae409-110">Как правило, это подходит для нераспределенных приложений.</span><span class="sxs-lookup"><span data-stu-id="ae409-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="ae409-111">Однако этот стиль программирования создает более сложный код поддержки RPC.</span><span class="sxs-lookup"><span data-stu-id="ae409-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="ae409-112">Заглушки клиента и сервера потребовали дополнительного кода для управления данными и указателями.</span><span class="sxs-lookup"><span data-stu-id="ae409-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="ae409-113">Базовый код заглушки должен разрешать различные указатели на адреса и определять, какая копия данных представляет самую последнюю версию.</span><span class="sxs-lookup"><span data-stu-id="ae409-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="ae409-114">Объем обработки можно уменьшить, если вы гарантируете, что указатель является единственным способом, которым приложение может получить доступ к области памяти.</span><span class="sxs-lookup"><span data-stu-id="ae409-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="ae409-115">Указатель может по-прежнему иметь множество функций указателя C.</span><span class="sxs-lookup"><span data-stu-id="ae409-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="ae409-116">Например, он может изменяться между значениями **null** и отличными от **null** или остаться одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="ae409-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="ae409-117">Это показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="ae409-117">The following example illustrates this.</span></span> <span data-ttu-id="ae409-118">Указатель имеет **значение NULL** перед вызовом и указывает на допустимую строку после вызова:</span><span class="sxs-lookup"><span data-stu-id="ae409-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![изменение указателя между значениями NULL и не NULL](images/prog-a01.png)

<span data-ttu-id="ae409-120">По умолчанию компилятор MIDL применяет \[ [уникальный](/windows/desktop/Midl/unique) \] атрибут указателя ко всем указателям, которые не являются параметрами.</span><span class="sxs-lookup"><span data-stu-id="ae409-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="ae409-121">Этот параметр по умолчанию можно изменить с помощью \[ атрибута [указателя \_ по умолчанию](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="ae409-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="ae409-122">Уникальный указатель имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="ae409-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="ae409-123">Оно может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ae409-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="ae409-124">При вызове может измениться со **значения NULL на значение** , отличное **от NULL.**</span><span class="sxs-lookup"><span data-stu-id="ae409-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="ae409-125">При изменении значения, отличного от **null**, выделяется новая память при возврате.</span><span class="sxs-lookup"><span data-stu-id="ae409-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="ae409-126">Во время вызова он может измениться с **значения** , отличного от **null** , на null.</span><span class="sxs-lookup"><span data-stu-id="ae409-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="ae409-127">Когда значение изменяется на **null**, приложение отвечает за освобождение памяти.</span><span class="sxs-lookup"><span data-stu-id="ae409-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="ae409-128">Значение может изменяться от одного значения, отличного от **null** , к другому.</span><span class="sxs-lookup"><span data-stu-id="ae409-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="ae409-129">Хранилище, на которое указывает уникальный указатель, не может быть получено любым другим указателем или именем в операции.</span><span class="sxs-lookup"><span data-stu-id="ae409-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="ae409-130">Возвращаемые данные записываются в существующее хранилище, если указатель не имеет значения **null**.</span><span class="sxs-lookup"><span data-stu-id="ae409-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="ae409-131">В следующем примере показано, как определить уникальный указатель.</span><span class="sxs-lookup"><span data-stu-id="ae409-131">The following example demonstrates how to define a unique pointer.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

<span data-ttu-id="ae409-132">В этом примере параметр *платежи ACH* является уникальным указателем на символьные данные, которые отправляются на сервер для обработки с помощью подпрограммы ремотефн.</span><span class="sxs-lookup"><span data-stu-id="ae409-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 