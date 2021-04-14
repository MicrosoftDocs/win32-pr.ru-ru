---
title: Метод OnConnect Имстскаксевентс
description: Вызывается, когда клиентский элемент управления начинает подключаться к серверу в ответ на вызов Имстскакс Connect.
ms.assetid: c5e367a8-126a-48bb-bc94-1063f77e8239
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnConnect
- Метод OnConnect службы удаленных рабочих столов, интерфейс Имстскаксевентс
- Интерфейс Имстскаксевентс службы удаленных рабочих столов, метод OnConnect
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2004fde83b79aff7b7c5082562de94f943eacb25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414749"
---
# <a name="imstscaxeventsonconnecting-method"></a>Метод Имстскаксевентс:: OnConnect

Вызывается, когда клиентский элемент управления начинает подключаться к серверу в ответ на вызов [**имстскакс:: Connect**](imstscax-connect.md).

## <a name="syntax"></a>Синтаксис


```C++
void OnConnecting();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Реализуйте этот метод в приемнике событий, чтобы получить уведомление о начале подключения элемента управления.

## <a name="examples"></a>Примеры

В следующем примере показано, как обрабатывает это событие с помощью Visual Basic кода скрипта. В этом примере предполагается, что управляющий объект называется "Мсрдпклиент".

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).


```VB
Sub MsRdpClient.OnConnecting()
    Msgbox("Connecting")
End sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имстскаксевентс**](imstscaxevents-interface.md)
</dt> </dl>

 

 





