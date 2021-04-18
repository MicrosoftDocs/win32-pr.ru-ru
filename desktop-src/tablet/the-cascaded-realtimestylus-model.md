---
description: Общие сведения о каскадной модели для класса RealTimeStylus.
ms.assetid: f4c377a7-979d-4a06-a8de-31b8e67d74f8
title: Модель каскадного RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2f61ea3cd44753d1d91fb2662226a716ee5590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561469"
---
# <a name="the-cascaded-realtimestylus-model"></a><span data-ttu-id="61a75-103">Модель каскадного RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="61a75-103">The Cascaded RealTimeStylus Model</span></span>

<span data-ttu-id="61a75-104">Каскадная модель [**RealTimeStylus**](realtimestylus-class.md) позволяет использовать два объекта **RealTimeStylus** , каждый из которых выполняется в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="61a75-104">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model enables you to use two **RealTimeStylus** objects, each running on a different thread.</span></span> <span data-ttu-id="61a75-105">В этой модели вы подключаете дополнительный объект **RealTimeStylus** к основному объекту **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-105">With this model, you attach a secondary **RealTimeStylus** object to a primary **RealTimeStylus** object.</span></span> <span data-ttu-id="61a75-106">Дополнительный объект **RealTimeStylus** присоединяется как единственный асинхронный подключаемый модуль в асинхронной коллекции подключаемых модулей объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-106">The secondary **RealTimeStylus** object is attached as the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>

<span data-ttu-id="61a75-107">Каскадная модель [**RealTimeStylus**](realtimestylus-class.md) может быть полезна в следующих сценариях.</span><span class="sxs-lookup"><span data-stu-id="61a75-107">The cascaded [**RealTimeStylus**](realtimestylus-class.md) model may be useful in the following scenarios.</span></span>

-   <span data-ttu-id="61a75-108">Вы можете добавить определенные задачи, которые могут быть необходимы для вычисления, но по-прежнему требуют доступа в режиме реального времени к потоку данных пера планшета, такому как распознавание жестов многоштриха, в синхронную коллекцию подключаемых модулей объекта [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="61a75-108">You can add certain tasks that may be computationally demanding yet still require real-time access to the tablet pen's data stream, such as multistroke gesture recognition, to the secondary [**RealTimeStylus**](realtimestylus-class.md) object's synchronous plug-in collection.</span></span>
-   <span data-ttu-id="61a75-109">Вычислительную нагрузку на синхронные подключаемые модули можно распределить по двум потокам, уменьшая задержки в сборе рукописных данных на некоторых планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="61a75-109">You can spread the computational load of your synchronous plug-ins over two threads, reducing delays in ink collection on some Tablet PCs.</span></span>

<span data-ttu-id="61a75-110">На следующей схеме показан поток данных пера планшета через два каскадных объекта [**RealTimeStylus**](realtimestylus-class.md) и их коллекции подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="61a75-110">The following diagram illustrates the flow of tablet pen data through two cascaded [**RealTimeStylus**](realtimestylus-class.md) objects and their plug-in collections.</span></span>

![Иллюстрация, показывающая каскадный поток данных RealTimeStylus](images/72ca1999-e078-49f8-a336-3b4d0157a472.gif)

<span data-ttu-id="61a75-112">На этой схеме круг с буквой "A" представляет данные пера планшета, которые уже обработаны как в первичном, так и во вторичном объектах [**RealTimeStylus**](realtimestylus-class.md) и были помещены в очередь вывода дополнительного объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-112">In this diagram the circle lettered "A" represents tablet pen data that has already been processed by both the primary and secondary [**RealTimeStylus**](realtimestylus-class.md) objects and has been placed on the secondary **RealTimeStylus** object's output queue.</span></span> <span data-ttu-id="61a75-113">Кружок с буквой "B" представляет данные пера планшета, которые уже были обработаны основным объектом **RealTimeStylus** и добавлены в очередь **вывода основного объекта RealTimeStylus и** еще не отправлены в дополнительный объект **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-113">The circle lettered "B" represents tablet pen data that has already been processed by the primary **RealTimeStylus** object and added to the primary **RealTimeStylus** object's output queue and has not yet been sent to the secondary **RealTimeStylus** object.</span></span> <span data-ttu-id="61a75-114">Кружок с буквой "C" представляет данные пера планшета, которые в настоящее время обрабатывает основной объект **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-114">The circle lettered "C" represents the tablet pen data that the primary **RealTimeStylus** object is currently processing.</span></span> <span data-ttu-id="61a75-115">Он отправляется в коллекцию синхронных подключаемых модулей и помещается в очередь вывода.</span><span class="sxs-lookup"><span data-stu-id="61a75-115">It is sent to the synchronous plug-in collection and placed on the output queue.</span></span> <span data-ttu-id="61a75-116">Пустой кружок представляет позицию в очереди вывода, в которой добавляются будущие данные пера планшета.</span><span class="sxs-lookup"><span data-stu-id="61a75-116">The empty circle represents the position in the output queue where future tablet pen data is added.</span></span>

## <a name="constraints"></a><span data-ttu-id="61a75-117">Ограничения</span><span class="sxs-lookup"><span data-stu-id="61a75-117">Constraints</span></span>

<span data-ttu-id="61a75-118">При использовании конструктора [**RealTimeStylus**](realtimestylus-class.md) по умолчанию создается объект **RealTimeStylus** , который может принимать только входные данные другого объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-118">If you use the default [**RealTimeStylus**](realtimestylus-class.md) constructor, you create a **RealTimeStylus** object that can only accept input from another **RealTimeStylus** object.</span></span>

<span data-ttu-id="61a75-119">В следующем списке описаны ограничения, связанные с использованием каскадной модели [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="61a75-119">The following list describes the constraints associated with using the cascaded [**RealTimeStylus**](realtimestylus-class.md) model.</span></span>

-   <span data-ttu-id="61a75-120">Можно использовать только два объекта [**RealTimeStylus**](realtimestylus-class.md) **: основной и дополнительный объекты** **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-120">Only two [**RealTimeStylus**](realtimestylus-class.md) objects may be used, a primary **RealTimeStylus** object and a secondary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="61a75-121">Основной объект [**RealTimeStylus**](realtimestylus-class.md) должен быть создан с помощью конструктора, использующего параметр **аттачедконтрол** или *Handle* .</span><span class="sxs-lookup"><span data-stu-id="61a75-121">The primary [**RealTimeStylus**](realtimestylus-class.md) object must be created with a constructor that uses the **attachedControl** or *handle* parameter.</span></span> <span data-ttu-id="61a75-122">Дополнительный объект **RealTimeStylus** должен быть создан с помощью конструктора без аргументов.</span><span class="sxs-lookup"><span data-stu-id="61a75-122">The secondary **RealTimeStylus** object must be created with the no-argument constructor.</span></span>
-   <span data-ttu-id="61a75-123">Дополнительный объект [**RealTimeStylus**](realtimestylus-class.md) должен быть единственным асинхронным подключаемым модулем в асинхронной коллекции подключаемых модулей объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-123">The secondary [**RealTimeStylus**](realtimestylus-class.md) object must be the only asynchronous plug-in in the primary **RealTimeStylus** object's asynchronous plug-in collection.</span></span>
-   <span data-ttu-id="61a75-124">Дополнительный объект [**RealTimeStylus**](realtimestylus-class.md) может быть присоединен только к одному первичному объекту **RealTimeStylus** за раз.</span><span class="sxs-lookup"><span data-stu-id="61a75-124">A secondary [**RealTimeStylus**](realtimestylus-class.md) object can only be attached to one primary **RealTimeStylus** object at a time.</span></span> <span data-ttu-id="61a75-125">Если он добавляется во второй Первичный объект **RealTimeStylus** , метод [Add](/previous-versions/ms824814(v=msdn.10)) создает исключение, а дополнительный объект **RealTimeStylus** не присоединяется к второму основному объекту **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-125">If it is added to a second primary **RealTimeStylus** object, the [Add](/previous-versions/ms824814(v=msdn.10)) method throws an exception, and the secondary **RealTimeStylus** object is not attached to the second primary **RealTimeStylus** object.</span></span>
-   <span data-ttu-id="61a75-126">Происходит изменение поведения некоторых членов объекта [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="61a75-126">The behavior of some of the secondary [**RealTimeStylus**](realtimestylus-class.md) object's members is modified.</span></span> <span data-ttu-id="61a75-127">В следующей таблице описывается измененное поведение этих элементов.</span><span class="sxs-lookup"><span data-stu-id="61a75-127">The following table describes the modified behavior of these members.</span></span>

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="61a75-128">Член</span><span class="sxs-lookup"><span data-stu-id="61a75-128">Member</span></span></th>
    <th><span data-ttu-id="61a75-129">Поведение</span><span class="sxs-lookup"><span data-stu-id="61a75-129">Behavior</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="61a75-130"><a href="/previous-versions/ms825905(v=msdn.10)">жетдесиредпаккетдескриптион</a></span><span class="sxs-lookup"><span data-stu-id="61a75-130"><a href="/previous-versions/ms825905(v=msdn.10)">GetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="61a75-131">Этот метод возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-131">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="61a75-132">Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , этот метод возвращает значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a75-132">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns the default value.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="61a75-133"><a href="/previous-versions/ms826041(v=msdn.10)">сетдесиредпаккетдескриптион</a></span><span class="sxs-lookup"><span data-stu-id="61a75-133"><a href="/previous-versions/ms826041(v=msdn.10)">SetDesiredPacketDescription</a></span></span></td>
    <td><span data-ttu-id="61a75-134">Этот метод вызывает исключение <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-134">This method raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span><br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="61a75-135"><a href="/previous-versions/ms825913(v=msdn.10)">Перо</a></span><span class="sxs-lookup"><span data-stu-id="61a75-135"><a href="/previous-versions/ms825913(v=msdn.10)">GetStyluses</a></span></span></td>
    <td><span data-ttu-id="61a75-136">Этот метод возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-136">This method returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="61a75-137">Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , этот метод возвращает пустой массив.</span><span class="sxs-lookup"><span data-stu-id="61a75-137">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, this method returns an empty array.</span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="61a75-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span><span class="sxs-lookup"><span data-stu-id="61a75-138"><a href="/previous-versions/ms824832(v=msdn.10)">Enabled</a></span></span></td>
    <td><span data-ttu-id="61a75-139">Получение этого свойства возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-139">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="61a75-140">Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , то получение этого свойства возвращает значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a75-140">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="61a75-141">Задание этого свойства вызывает исключение <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-141">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="61a75-142"><a href="/previous-versions/ms824834(v=msdn.10)">виндовинпутректангле</a></span><span class="sxs-lookup"><span data-stu-id="61a75-142"><a href="/previous-versions/ms824834(v=msdn.10)">WindowInputRectangle</a></span></span></td>
    <td><span data-ttu-id="61a75-143">Получение этого свойства возвращает сведения из основного объекта <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-143">Getting this property returns the information from the primary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> object.</span></span><br/> <span data-ttu-id="61a75-144">Если дополнительный объект <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> не присоединен к основному объекту <strong>RealTimeStylus</strong> , то получение этого свойства возвращает значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="61a75-144">If the secondary <a href="realtimestylus-class.md"><strong>RealTimeStylus</strong></a> is not attached to a primary <strong>RealTimeStylus</strong> object, getting this property returns the default value.</span></span><br/>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="61a75-145">Задание этого свойства вызывает исключение <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> .</span><span class="sxs-lookup"><span data-stu-id="61a75-145">Setting this property raises an <a href="/dotnet/api/system.invalidoperationexception">InvalidOperationException</a> exception.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="61a75-146">Родительский объект [**RealTimeStylus**](realtimestylus-class.md) должен перестать работать при удалении дочернего объекта **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="61a75-146">The parent [**RealTimeStylus**](realtimestylus-class.md) object is expected to stop functioning when the child **RealTimeStylus** is Disposed.</span></span>

 

 
