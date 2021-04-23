---
description: Удаление экземпляра — это наиболее распространенная команда удаления, которая, скорее всего, будет выполняться в инструментарии WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Удаление экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702073"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="94c48-103">Удаление экземпляра</span><span class="sxs-lookup"><span data-stu-id="94c48-103">Deleting an Instance</span></span>

<span data-ttu-id="94c48-104">Удаление экземпляра — это наиболее распространенная команда удаления, которая, скорее всего, будет выполняться в инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="94c48-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="94c48-105">Как и при удалении класса, фактическая команда довольно проста.</span><span class="sxs-lookup"><span data-stu-id="94c48-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="94c48-106">Однако Инструментарий WMI работает совершенно иначе в зависимости от типа удаляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="94c48-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="94c48-107">Если экземпляр является статическим, Инструментарий WMI просто удаляет экземпляр из репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="94c48-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="94c48-108">Сведения об удалении классов и экземпляров из репозитория WMI см. в описании команды препроцессора [**pragma делетекласс**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="94c48-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="94c48-109">Если экземпляр является динамическим, Инструментарий WMI должен вызвать [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) для поставщиков, ответственных за следующие классы:</span><span class="sxs-lookup"><span data-stu-id="94c48-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="94c48-110">Класс, которому принадлежит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="94c48-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="94c48-111">Каждый родительский класс класса, владеющего экземпляром.</span><span class="sxs-lookup"><span data-stu-id="94c48-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="94c48-112">Каждый подкласс класса, владеющего экземпляром.</span><span class="sxs-lookup"><span data-stu-id="94c48-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="94c48-113">Успешность удаления зависит от самого верхнего неабстрактного класса для исходного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="94c48-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="94c48-114">Если поставщик любого самого верхнего неабстрактного класса успешно завершает удаление, операция завершается успешно.</span><span class="sxs-lookup"><span data-stu-id="94c48-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="94c48-115">Дополнительные сведения см. в подразделе "Примечания" [**IWbemServices::D елетеинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span><span class="sxs-lookup"><span data-stu-id="94c48-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="94c48-116">[Интерфейс API COM для WMI](com-api-for-wmi.md) имеет различные методы для удаления экземпляра и удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="94c48-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="94c48-117">В следующей процедуре описывается, как использовать C++ для удаления экземпляра базового класса или производного класса.</span><span class="sxs-lookup"><span data-stu-id="94c48-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="94c48-118">**Удаление экземпляра базового класса или производного класса с помощью C++**</span><span class="sxs-lookup"><span data-stu-id="94c48-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="94c48-119">Вызовите методы [**IWbemServices::D елетеинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="94c48-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="94c48-120">Как видно из названия, [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) удаляет экземпляр асинхронно, в то время как [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) удаляет экземпляр синхронно.</span><span class="sxs-lookup"><span data-stu-id="94c48-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="94c48-121">Чтобы использовать **делетеинстанцеасинк**, необходимо также реализовать объект [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="94c48-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="94c48-122">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="94c48-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="94c48-123">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="94c48-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="94c48-124">[API скриптов для WMI](scripting-api-for-wmi.md) использует те же методы для удаления объекта класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="94c48-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="94c48-125">В следующей процедуре описывается, как использовать VBScript для удаления экземпляра базового класса или производного класса.</span><span class="sxs-lookup"><span data-stu-id="94c48-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="94c48-126">**Удаление экземпляра базового класса или производного класса с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="94c48-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="94c48-127">Вызовите методы [**SWbemObject. Delete \_**](swbemobject-delete-.md) или [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="94c48-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="94c48-128">Как видно из названия, [**DELETE \_**](swbemobject-delete-.md) удаляет экземпляр синхронно, в то время как [**DeleteAsync \_**](swbemobject-deleteasync-.md) удаляет экземпляр асинхронно.</span><span class="sxs-lookup"><span data-stu-id="94c48-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="94c48-129">Дополнительные сведения об асинхронном удалении экземпляра см. в разделе [вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="94c48-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="94c48-130">В следующем примере показано, как удалить экземпляр с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="94c48-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="94c48-131">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="94c48-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="94c48-132">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="94c48-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



