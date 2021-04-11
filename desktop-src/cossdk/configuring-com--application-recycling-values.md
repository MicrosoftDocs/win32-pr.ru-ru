---
description: Для настройки значений перезапуска приложения COM+ можно использовать следующие методы.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Настройка значений перезапуска приложения COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142616"
---
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="3c4b7-103">Настройка значений перезапуска приложения COM+</span><span class="sxs-lookup"><span data-stu-id="3c4b7-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="3c4b7-104">Для настройки значений перезапуска приложения COM+ можно использовать следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="3c4b7-105">Нельзя перезапустить приложение COM+, настроенное для запуска в качестве службы Windows.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="3c4b7-106">Кроме того, библиотечные приложения имеют свойства перезапуска и группирования для своего хостового процесса.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3c4b7-107">Средство администрирования служб компонентов</span><span class="sxs-lookup"><span data-stu-id="3c4b7-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="3c4b7-108">Чтобы настроить перезапуск приложения для приложения COM+, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="3c4b7-109">В дереве консоли средства администрирования "службы компонентов" щелкните правой кнопкой мыши серверное приложение COM+, которое необходимо перезапустить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="3c4b7-110">На вкладке **пулы & перезапуск** введите значения для **предельного времени жизни (в минутах)**, **предела памяти (КБ)**, **времени ожидания (в минутах)**, **предельного числа вызовов** и **ограничения активации** в зависимости от критериев, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="3c4b7-111">**Ограничение времени существования** указывает максимальное число минут, в течение которых процесс может быть выполнен до его перезапуска.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="3c4b7-112">Допустимый диапазон — от 0 до 30 240 минут (21 день).</span><span class="sxs-lookup"><span data-stu-id="3c4b7-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="3c4b7-113">Число минут по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="3c4b7-114">**Ограничение памяти** указывает максимальный объем использования памяти процесса (в килобайтах) перед повторным запуском процесса.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="3c4b7-115">Если объем используемой памяти процесса превышает указанное число в течение более одной минуты, процесс перезапускается.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="3c4b7-116">Допустимый диапазон — от 0 до 1 048 576 КБ, а объем используемой памяти по умолчанию — 0 КБ.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="3c4b7-117">**Время ожидания окончания срока действия** указывает количество минут ожидания, прежде чем принудительно завершить работу, для выпуска всех внешних ссылок на объекты в процессе.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="3c4b7-118">Допустимый диапазон — от 1 до 1440 минут (24 часа), а время ожидания истечения срока действия по умолчанию — 15 минут.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="3c4b7-119">Это значение используется только в том случае, если уже определено, что процесс будет перезапущен на основе других критериев.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="3c4b7-120">**Ограничение вызовов** указывает максимальное число вызовов, которые могут быть приняты объектами приложения перед повторным запуском процесса.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="3c4b7-121">Допустимый диапазон — от 0 до 1 048 576 вызовов, а число вызовов по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="3c4b7-122">**Ограничение активации** указывает максимальное число активаций объекта приложения, которое следует принять перед повторным запуском процесса.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="3c4b7-123">Допустимый диапазон — от 0 до 1 048 576 активаций, а число активаций по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="3c4b7-124">Если **предельное значение времени жизни**, **ограничение памяти**, **число вызовов** или **ограничение активации** задано равным 0 (значение по умолчанию), перезапуск приложения для этого критерия отключается.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="3c4b7-125">Если все четыре условия имеют значение 0, повторное использование приложений для выбранного приложения отключается.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="3c4b7-126">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3c4b7-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3c4b7-127">Visual Basic</span></span>

<span data-ttu-id="3c4b7-128">В следующей функции Microsoft Visual Basic показано, как можно задать значения для повторного запуска приложения для любого выбранного серверного приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="3c4b7-129">Чтобы использовать его из Visual Basic, добавьте ссылку на библиотеку типов администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



<span data-ttu-id="3c4b7-130">Чтобы использовать функцию, укажите строковое значение для имени приложения и целочисленные значения для нужных параметров повторного запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="3c4b7-131">В следующем Visual Basic коде показано, как установить значение **рециклелифетимелимит** равным 5, значение **рециклемеморилимит** — 10, значение **Рециклекалллимит** — 9, значение **Рециклеактиватионлимит** — 100, а для параметра **RecycleExpirationTimeout** — значение 15.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="3c4b7-132">См. также</span><span class="sxs-lookup"><span data-stu-id="3c4b7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c4b7-133">Основные понятия перезапуска приложений COM+</span><span class="sxs-lookup"><span data-stu-id="3c4b7-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



