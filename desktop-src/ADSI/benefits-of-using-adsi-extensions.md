---
title: Преимущества использования расширений ADSI
description: Способ реализации методов расширения зависит от модуля записи расширений.
ms.assetid: dbd1a203-b94c-4739-8c9d-aed1c9b43426
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27e80e6c095fcc02ca02c57b0987d1e6ed410ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067335"
---
# <a name="benefits-of-using-adsi-extensions"></a><span data-ttu-id="3dccd-103">Преимущества использования расширений ADSI</span><span class="sxs-lookup"><span data-stu-id="3dccd-103">Benefits of Using ADSI Extensions</span></span>

<span data-ttu-id="3dccd-104">Способ реализации методов расширения зависит от модуля записи расширений.</span><span class="sxs-lookup"><span data-stu-id="3dccd-104">The way in which extension methods are implemented depends on the extension writer.</span></span> <span data-ttu-id="3dccd-105">Модуль записи расширений может даже реализовать метод полностью вне области действия каталога.</span><span class="sxs-lookup"><span data-stu-id="3dccd-105">An extension writer may even implement a method completely outside the scope of the directory.</span></span> <span data-ttu-id="3dccd-106">Например, разработчику резервных копий и восстановления программных планов можно расширить объект с именем **Computer**.</span><span class="sxs-lookup"><span data-stu-id="3dccd-106">For example, a developer of backup and restore software plans to extend an object called **computer**.</span></span> <span data-ttu-id="3dccd-107">Разработчик должен создать два метода: **резервное копирование** и **Восстановление**.</span><span class="sxs-lookup"><span data-stu-id="3dccd-107">The developer must create two methods: **BackUp** and **Restore**.</span></span> <span data-ttu-id="3dccd-108">Эти методы работают удаленно на физическом компьютере, на который указывает объект **компьютера** в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3dccd-108">These methods operate remotely on the physical computer that the **computer** object in the directory points to.</span></span> <span data-ttu-id="3dccd-109">Выполняя роль расширения, компонент обращается к инфраструктуре ADSI и просматривается клиентами ADSI как неотъемлемой частью объекта.</span><span class="sxs-lookup"><span data-stu-id="3dccd-109">By acting as an extension, the component accesses the ADSI infrastructure and is viewed by ADSI clients as an integral part of the object.</span></span>

<span data-ttu-id="3dccd-110">В следующих сценариях описываются ситуации, когда создание расширения для ADSI будет выгодно:</span><span class="sxs-lookup"><span data-stu-id="3dccd-110">The following scenarios describe situations where creating an extension to ADSI would be advantageous:</span></span>

-   <span data-ttu-id="3dccd-111">Создайте расширение для интеграции компонента с объектом каталога.</span><span class="sxs-lookup"><span data-stu-id="3dccd-111">Create an extension to integrate a component with the directory object.</span></span> <span data-ttu-id="3dccd-112">Поскольку в каталоге имеется объект **пользователя** , РАЗРАБОТЧИКУ отдела кадров может потребоваться создать расширение ADSI, которое заполняет другие данные в каталоге при создании **пользователя** .</span><span class="sxs-lookup"><span data-stu-id="3dccd-112">Because there is a **user** object in the directory, an HR developer may wish to create an ADSI extension that populates other data in the directory when a **user** is created.</span></span>
-   <span data-ttu-id="3dccd-113">Создайте расширение, если для компонента требуется поиск в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3dccd-113">Create an extension if a component requires a directory lookup.</span></span> <span data-ttu-id="3dccd-114">Компоненту может потребоваться каталог в качестве отправной точки для поиска.</span><span class="sxs-lookup"><span data-stu-id="3dccd-114">A component may require a directory as a starting point for a lookup.</span></span> <span data-ttu-id="3dccd-115">Например, при создании нового приложения.</span><span class="sxs-lookup"><span data-stu-id="3dccd-115">For example, when creating a new application.</span></span> <span data-ttu-id="3dccd-116">Объект приложения **тулапп** можно опубликовать в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3dccd-116">An application object, **ToolApp**, can be published in the directory.</span></span> <span data-ttu-id="3dccd-117">Приложение может поддерживать уведомления о состоянии для коллекции почтовых серверов.</span><span class="sxs-lookup"><span data-stu-id="3dccd-117">Your application may support status notifications on a collection of mail servers.</span></span> <span data-ttu-id="3dccd-118">Вы решили сделать это приложение расширением ADSI.</span><span class="sxs-lookup"><span data-stu-id="3dccd-118">You decide to make this application an ADSI extension.</span></span>

    <span data-ttu-id="3dccd-119">Теперь пользователь может искать все экземпляры **тулапп** в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3dccd-119">Now, a user may search for all instances of **ToolApp** in the directory.</span></span> <span data-ttu-id="3dccd-120">Для каждого возвращаемого объекта пользователь может выдать вызов **нотифинов ()**.</span><span class="sxs-lookup"><span data-stu-id="3dccd-120">For each object returned, the user may issue a call to **NotifyNow()**.</span></span> <span data-ttu-id="3dccd-121">Приложение или расширение может получать в каталоге больше текущих данных объектов и уведомлять каждый сервер асинхронно.</span><span class="sxs-lookup"><span data-stu-id="3dccd-121">An application or extension can obtain more current object data in the directory and notify each server asynchronously.</span></span>

-   <span data-ttu-id="3dccd-122">Создайте расширение как соединение между пространствами имен и моделями программирования.</span><span class="sxs-lookup"><span data-stu-id="3dccd-122">Create an extension as a junction between namespaces and programming models.</span></span> <span data-ttu-id="3dccd-123">Например, ISV проводит новую объектную модель для служб печати.</span><span class="sxs-lookup"><span data-stu-id="3dccd-123">For example, an ISV invents a new object model for print services.</span></span> <span data-ttu-id="3dccd-124">Объект **очереди печати** уже определен в каталоге.</span><span class="sxs-lookup"><span data-stu-id="3dccd-124">The **printQueue** object is already defined in the directory.</span></span> <span data-ttu-id="3dccd-125">Независимый поставщик программного обеспечения может создать расширение ADSI и связать его с объектом **очереди печати** .</span><span class="sxs-lookup"><span data-stu-id="3dccd-125">The ISV can create an ADSI extension and associate it with the **printQueue** object.</span></span> <span data-ttu-id="3dccd-126">Пользователи ADSI могут выполнить привязку к объекту **очереди печати** и начать использовать объектную модель для независимого поставщика программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3dccd-126">ADSI users can bind to a **printQueue** object and start using the object model for the ISV.</span></span> <span data-ttu-id="3dccd-127">С точки зрения клиента ADSI эта точка соединения прозрачна.</span><span class="sxs-lookup"><span data-stu-id="3dccd-127">From the ADSI client perspective, this junction point is transparent.</span></span>
-   <span data-ttu-id="3dccd-128">Создайте расширение для упрощения задач.</span><span class="sxs-lookup"><span data-stu-id="3dccd-128">Create an extension to simplify tasks.</span></span> <span data-ttu-id="3dccd-129">Многие задачи в каталоге могут быть выполнены путем поиска и установки нескольких атрибутов в объекте или нескольких объектах.</span><span class="sxs-lookup"><span data-stu-id="3dccd-129">Many tasks in the directory can be accomplished by searching and setting multiple attributes in an object or multiple objects.</span></span> <span data-ttu-id="3dccd-130">Создание одной функции для управления несколькими атрибутами упрощает разработку для модулей записи приложений и сценариев.</span><span class="sxs-lookup"><span data-stu-id="3dccd-130">By creating a single function to manipulate multiple attributes, it simplifies development for application and script writers.</span></span>

<span data-ttu-id="3dccd-131">Расширения для клиентов ADSI расширяют среду программирования ADSI несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="3dccd-131">For ADSI clients, extensions enrich the ADSI programming environment in several ways:</span></span>

-   <span data-ttu-id="3dccd-132">Разработчикам, создающим клиенты ADSI, не нужно изучать новую модель программирования.</span><span class="sxs-lookup"><span data-stu-id="3dccd-132">Developers creating ADSI clients do not have to learn a new programming model.</span></span> <span data-ttu-id="3dccd-133">Расширения являются частью ADSI.</span><span class="sxs-lookup"><span data-stu-id="3dccd-133">The extensions are part of ADSI.</span></span> <span data-ttu-id="3dccd-134">Они будут использовать ту же парадигму для поиска, обработки данных и защиты объектов.</span><span class="sxs-lookup"><span data-stu-id="3dccd-134">They would use the same paradigm for searching, data manipulation, and securing objects.</span></span>
-   <span data-ttu-id="3dccd-135">Администраторы могут управлять связанными приложениями, поддерживающими каталоги, с помощью расширений.</span><span class="sxs-lookup"><span data-stu-id="3dccd-135">Administrators can manage related directory-enabled applications using extensions.</span></span>
-   <span data-ttu-id="3dccd-136">Потребители расширений могут просматривать объект ADSI и расширение как один интегрированный объект.</span><span class="sxs-lookup"><span data-stu-id="3dccd-136">Extension consumers can view an ADSI object and extension as one integrated object.</span></span>
-   <span data-ttu-id="3dccd-137">Существующие компоненты могут быть интегрированы с интерфейсом ADSI, что позволяет расширениям использовать существующие инвестиции и создавать взаимосвязи между компонентами.</span><span class="sxs-lookup"><span data-stu-id="3dccd-137">Existing components may be integrated with ADSI, which enables extensions to leverage existing investments and create synergy between components.</span></span>

<span data-ttu-id="3dccd-138">Расширения ADSI разработаны со следующими целями:</span><span class="sxs-lookup"><span data-stu-id="3dccd-138">ADSI extensions were designed with the following objectives:</span></span>

-   <span data-ttu-id="3dccd-139">Простота реализации.</span><span class="sxs-lookup"><span data-stu-id="3dccd-139">Easy to implement.</span></span> <span data-ttu-id="3dccd-140">С текущими существующими технологиями Майкрософт, системой разработки Microsoft Visual C++ и библиотекой активных шаблонов можно быстро создать расширение.</span><span class="sxs-lookup"><span data-stu-id="3dccd-140">With the current existing Microsoft technologies, Microsoft Visual C++ development system, and the Active Template Library, an extension can be created quickly.</span></span>
-   <span data-ttu-id="3dccd-141">Клиенты просматривают один IDispatch.</span><span class="sxs-lookup"><span data-stu-id="3dccd-141">Clients view one IDispatch.</span></span> <span data-ttu-id="3dccd-142">С точки зрения сценариев и модулей записи автоматизации, методы и свойства расширения прозрачно смешиваются в один объект ADSI.</span><span class="sxs-lookup"><span data-stu-id="3dccd-142">From the perspective of script and Automation writers, the extension methods and properties are transparently blended into one ADSI object.</span></span>
-   <span data-ttu-id="3dccd-143">Независимых.</span><span class="sxs-lookup"><span data-stu-id="3dccd-143">Independent.</span></span> <span data-ttu-id="3dccd-144">Модули записи расширений могут независимо расширять интерфейсы ADSI без предварительного знания существующих расширений.</span><span class="sxs-lookup"><span data-stu-id="3dccd-144">Extension writers can independently extend ADSI without prior knowledge of existing extensions.</span></span>

<span data-ttu-id="3dccd-145">Рассмотрим этот сценарий: корпоративному разработчику или поставщику программного обеспечения требуется разработать программу резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3dccd-145">Consider this scenario: A corporate developer or an ISV needs to develop a backup program.</span></span> <span data-ttu-id="3dccd-146">Это приложение резервного копирования позволяет администратору выполнять резервное копирование всех компьютеров в подразделении.</span><span class="sxs-lookup"><span data-stu-id="3dccd-146">This backup application enables an administrator to back up all computers in an organizational unit.</span></span> <span data-ttu-id="3dccd-147">С расширением ADSI возможны следующие сценарии.</span><span class="sxs-lookup"><span data-stu-id="3dccd-147">With an ADSI extension, the following script is possible.</span></span>


```VB
Dim ou
On Error Resume Next
Set ou = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
If Err.Number<>0 Then
    MsgBox("An error has occurred.")
    Err.Clear
    Set ou = Nothing
    Exit Sub
End If

ou.Filter = Array("computer")

For each comp in ou
   Debug.Print comp.Get("networkAddress")
   Debug.Print comp.LastBackUp
   comp.BackUpNow
Next
```



<span data-ttu-id="3dccd-148">**Ластбаккуп** — это свойство, а **кнопка** — это метод, предоставляемый модулем записи расширений.</span><span class="sxs-lookup"><span data-stu-id="3dccd-148">**LastBackUp** is a property and **BackUpNow** is a method that the extension writer provides.</span></span> <span data-ttu-id="3dccd-149">В коде показаны преимущества для потребителей и поставщиков расширений.</span><span class="sxs-lookup"><span data-stu-id="3dccd-149">The code shows the benefits for both extension consumers and providers.</span></span> <span data-ttu-id="3dccd-150">Модуль записи расширений не должен создавать новый способ фильтрации, поиска и доступа к каталогу.</span><span class="sxs-lookup"><span data-stu-id="3dccd-150">The extension writer does not have to create a new way of filtering, searching, and accessing the directory.</span></span> <span data-ttu-id="3dccd-151">Потребителю расширения не нужно переучить новую парадигму программирования.</span><span class="sxs-lookup"><span data-stu-id="3dccd-151">The extension consumer does not have to relearn a new programming paradigm.</span></span> <span data-ttu-id="3dccd-152">Новые методы и свойства, предоставляемые модулем записи расширений, просматриваются как часть ADSI.</span><span class="sxs-lookup"><span data-stu-id="3dccd-152">New methods and properties that the extension writer provides are viewed as part of ADSI.</span></span>

 

 




