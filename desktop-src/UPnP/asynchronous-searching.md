---
title: Асинхронный поиск
description: Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск. Асинхронный поиск немедленно возвращает управление вызывающему приложению.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3482e041798db929d1719e1a404823f161f9bf5b0e499f4eca1694df24b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058142"
---
# <a name="asynchronous-searching"></a>Асинхронный поиск

Объект Finder устройства обеспечивает как синхронный, так и асинхронный поиск. Асинхронный поиск немедленно возвращает управление вызывающему приложению. Затем приложение уведомляет о каждом отдельном устройстве по мере его обнаружения, используя интерфейс обратного вызова, зарегистрированный приложением.

Асинхронный поиск лучше подходит для графических интерфейсов пользователя и приложений, выполняющих непрерывный мониторинг.

Общая структура асинхронного поиска:

1.  Создание объекта поиска
2.  Начать поиск
3.  Получение уведомлений обратного вызова и выполнение соответствующих действий по обработке.
4.  Если поиск больше не нужен, отмените поиск и освободите связанные объекты.

> [!Note]  
> В коде обратного вызова приложение не может освободить объект, о котором получает уведомление, например новое устройство, и приложение не может отменить поиск.

 

## <a name="c-example"></a>Пример C++

Приложения C++ должны реализовывать объект обратного вызова для передачи в поиск. Пример кода, иллюстрирующий это действие, см. [в разделе Асинхронный поиск в C++](searching-asynchronously-in-c-.md) .

## <a name="vbscript-example"></a>Пример VBScript

Код VBScript должен передавать адрес функции обратного вызова.


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



 

 




