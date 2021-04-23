---
title: Асинхронный поиск
description: Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск. Асинхронный поиск немедленно возвращает управление вызывающему приложению.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986753"
---
# <a name="asynchronous-searching"></a><span data-ttu-id="a7187-104">Асинхронный поиск</span><span class="sxs-lookup"><span data-stu-id="a7187-104">Asynchronous Searching</span></span>

<span data-ttu-id="a7187-105">Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск.</span><span class="sxs-lookup"><span data-stu-id="a7187-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="a7187-106">Асинхронный поиск немедленно возвращает управление вызывающему приложению.</span><span class="sxs-lookup"><span data-stu-id="a7187-106">Asynchronous searches return control to the calling application immediately.</span></span> <span data-ttu-id="a7187-107">Затем приложение уведомляет о каждом отдельном устройстве по мере его обнаружения, используя интерфейс обратного вызова, зарегистрированный приложением.</span><span class="sxs-lookup"><span data-stu-id="a7187-107">Then, the application is notified about each individual device as it is found, using a callback interface that the application has registered.</span></span>

<span data-ttu-id="a7187-108">Асинхронный поиск лучше подходит для графических интерфейсов пользователя и приложений, выполняющих непрерывный мониторинг.</span><span class="sxs-lookup"><span data-stu-id="a7187-108">Asynchronous searching is best for graphical user interfaces, and applications that perform continuous monitoring.</span></span>

<span data-ttu-id="a7187-109">Общая структура асинхронного поиска:</span><span class="sxs-lookup"><span data-stu-id="a7187-109">The general structure of an asynchronous search is:</span></span>

1.  <span data-ttu-id="a7187-110">Создание объекта поиска</span><span class="sxs-lookup"><span data-stu-id="a7187-110">Create a search object</span></span>
2.  <span data-ttu-id="a7187-111">Начать поиск</span><span class="sxs-lookup"><span data-stu-id="a7187-111">Start the search</span></span>
3.  <span data-ttu-id="a7187-112">Получение уведомлений обратного вызова и выполнение соответствующих действий по обработке.</span><span class="sxs-lookup"><span data-stu-id="a7187-112">Receive callback notifications and take the appropriate processing steps.</span></span>
4.  <span data-ttu-id="a7187-113">Если поиск больше не нужен, отмените поиск и освободите связанные объекты.</span><span class="sxs-lookup"><span data-stu-id="a7187-113">When the search is no longer needed, cancel the search and release the associated objects.</span></span>

> [!Note]  
> <span data-ttu-id="a7187-114">В коде обратного вызова приложение не может освободить объект, о котором получает уведомление, например новое устройство, и приложение не может отменить поиск.</span><span class="sxs-lookup"><span data-stu-id="a7187-114">In the callback code, an application cannot release the object it is receiving notification about, such as a new device, nor can the application cancel the search.</span></span>

 

## <a name="c-example"></a><span data-ttu-id="a7187-115">Пример C++</span><span class="sxs-lookup"><span data-stu-id="a7187-115">C++ Example</span></span>

<span data-ttu-id="a7187-116">Приложения C++ должны реализовывать объект обратного вызова для передачи в поиск.</span><span class="sxs-lookup"><span data-stu-id="a7187-116">C++ applications must implement a callback object to pass to the search.</span></span> <span data-ttu-id="a7187-117">Пример кода, иллюстрирующий это действие, см. [в разделе Асинхронный поиск в C++](searching-asynchronously-in-c-.md) .</span><span class="sxs-lookup"><span data-stu-id="a7187-117">See [Searching Asynchronously in C++](searching-asynchronously-in-c-.md) for sample code that illustrates this action.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="a7187-118">Пример VBScript</span><span class="sxs-lookup"><span data-stu-id="a7187-118">VBScript Example</span></span>

<span data-ttu-id="a7187-119">Код VBScript должен передавать адрес функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a7187-119">VBScript code must pass the address of the callback function.</span></span>


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




