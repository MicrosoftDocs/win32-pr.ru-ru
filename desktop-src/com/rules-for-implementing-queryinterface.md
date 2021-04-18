---
title: Правила реализации QueryInterface
description: Правила реализации QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700940"
---
# <a name="rules-for-implementing-queryinterface"></a><span data-ttu-id="b0d29-103">Правила реализации QueryInterface</span><span class="sxs-lookup"><span data-stu-id="b0d29-103">Rules for Implementing QueryInterface</span></span>

<span data-ttu-id="b0d29-104">Существует три основных правила, которые управляют реализацией метода [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для COM-объекта:</span><span class="sxs-lookup"><span data-stu-id="b0d29-104">There are three main rules that govern implementing the [**IUnknown::QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) method on a COM object:</span></span>

-   <span data-ttu-id="b0d29-105">Объекты должны иметь удостоверение.</span><span class="sxs-lookup"><span data-stu-id="b0d29-105">Objects must have identity.</span></span>
-   <span data-ttu-id="b0d29-106">Набор интерфейсов в экземпляре объекта должен быть статическим.</span><span class="sxs-lookup"><span data-stu-id="b0d29-106">The set of interfaces on an object instance must be static.</span></span>
-   <span data-ttu-id="b0d29-107">Для любого интерфейса объекта из любого другого интерфейса должно быть возможно успешное выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="b0d29-107">It must be possible to query successfully for any interface on an object from any other interface.</span></span>

## <a name="objects-must-have-identity"></a><span data-ttu-id="b0d29-108">Объекты должны иметь удостоверение</span><span class="sxs-lookup"><span data-stu-id="b0d29-108">Objects Must Have Identity</span></span>

<span data-ttu-id="b0d29-109">Для любого заданного экземпляра объекта вызов [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) с \_ интерфейсом IID IUnknown должен всегда возвращать одно и то же значение физического указателя.</span><span class="sxs-lookup"><span data-stu-id="b0d29-109">For any given object instance, a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) with IID\_IUnknown must always return the same physical pointer value.</span></span> <span data-ttu-id="b0d29-110">Это позволяет вызывать **QueryInterface** на любом из двух интерфейсов и сравнивать результаты, чтобы определить, указывают ли они на один и тот же экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="b0d29-110">This allows you to call **QueryInterface** on any two interfaces and compare the results to determine whether they point to the same instance of an object.</span></span>

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a><span data-ttu-id="b0d29-111">Набор интерфейсов в экземпляре объекта должен быть статическим</span><span class="sxs-lookup"><span data-stu-id="b0d29-111">The Set of Interfaces on an Object Instance Must Be Static</span></span>

<span data-ttu-id="b0d29-112">Набор интерфейсов, доступных для объекта через [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , должен быть статическим, а не динамическим.</span><span class="sxs-lookup"><span data-stu-id="b0d29-112">The set of interfaces accessible on an object through [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) must be static, not dynamic.</span></span> <span data-ttu-id="b0d29-113">В частности, если **QueryInterface** возвращает \_ "ОК" для заданного IID, он никогда не должен возвращать e \_ Interface при последующих вызовах для того же объекта; и если **QueryInterface** ВОЗВРАЩАЕТ e \_ -интерфейс для заданного IID, последующие вызовы для одного и того же идентификатора IID на одном и том же объекте не должны возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b0d29-113">Specifically, if **QueryInterface** returns S\_OK for a given IID once, it must never return E\_NOINTERFACE on subsequent calls on the same object; and if **QueryInterface** returns E\_NOINTERFACE for a given IID, subsequent calls for the same IID on the same object must never return S\_OK.</span></span>

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a><span data-ttu-id="b0d29-114">Для любого интерфейса объекта из любого другого интерфейса необходимо иметь возможность успешного выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="b0d29-114">It Must Be Possible to Query Successfully for Any Interface on an Object from Any Other Interface</span></span>

<span data-ttu-id="b0d29-115">Это происходит при наличии следующего кода:</span><span class="sxs-lookup"><span data-stu-id="b0d29-115">That is, given the following code:</span></span>

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

<span data-ttu-id="b0d29-116">применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="b0d29-116">the following rules apply:</span></span>

-   <span data-ttu-id="b0d29-117">Если у вас есть указатель на интерфейс в объекте, необходимо успешно вызвать метод [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для этого же интерфейса следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b0d29-117">If you have a pointer to an interface on an object, a call like the following to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for that same interface must succeed:</span></span>

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="b0d29-118">Если вызов [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) для второго указателя интерфейса завершился с ошибкой, вызов **QueryInterface** из этого указателя для первого интерфейса также должен быть выполнен.</span><span class="sxs-lookup"><span data-stu-id="b0d29-118">If a call to [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) for a second interface pointer succeeds, a call to **QueryInterface** from that pointer for the first interface must also succeed.</span></span> <span data-ttu-id="b0d29-119">Если удалось получить pB, также необходимо выполнить следующее:</span><span class="sxs-lookup"><span data-stu-id="b0d29-119">If pB was successfully obtained, the following must also succeed:</span></span>

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   <span data-ttu-id="b0d29-120">Любой интерфейс должен иметь возможность запрашивать любой другой интерфейс для объекта.</span><span class="sxs-lookup"><span data-stu-id="b0d29-120">Any interface must be able to query for any other interface on an object.</span></span> <span data-ttu-id="b0d29-121">Если запрос pB был успешно получен, и вы успешно запрашиваете третий интерфейс (IC) с помощью этого указателя, необходимо также иметь возможность успешного запроса для IC с помощью первого указателя, pA.</span><span class="sxs-lookup"><span data-stu-id="b0d29-121">If pB was successfully obtained and you successfully query for a third interface (IC) using that pointer, you must also be able to query successfully for IC using the first pointer, pA.</span></span> <span data-ttu-id="b0d29-122">В этом случае должна быть выполнена следующая последовательность:</span><span class="sxs-lookup"><span data-stu-id="b0d29-122">In this case, the following sequence must succeed:</span></span>

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

<span data-ttu-id="b0d29-123">Реализации интерфейса должны поддерживать Счетчик необработанных ссылок на указатели на все интерфейсы данного объекта.</span><span class="sxs-lookup"><span data-stu-id="b0d29-123">Interface implementations must maintain a counter of outstanding pointer references to all the interfaces on a given object.</span></span> <span data-ttu-id="b0d29-124">Для счетчика следует использовать **целое число без знака** .</span><span class="sxs-lookup"><span data-stu-id="b0d29-124">You should use an **unsigned integer** for the counter.</span></span>

<span data-ttu-id="b0d29-125">Если клиенту необходимо выяснить, что ресурсы были освобождены, то перед вызовом [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)необходимо использовать метод в интерфейсе объекта с семантикой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="b0d29-125">If a client needs to know that resources have been freed, it must use a method in some interface on the object with higher-level semantics before calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0d29-126">См. также</span><span class="sxs-lookup"><span data-stu-id="b0d29-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0d29-127">Использование и реализация IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0d29-127">Using and Implementing IUnknown</span></span>](using-and-implementing-iunknown.md)
</dt> </dl>

 

 