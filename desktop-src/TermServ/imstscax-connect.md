---
title: Имстскакс Connect, метод
description: Инициирует соединение с использованием свойств, заданных в данный момент в элементе управления.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Метод Connect службы удаленных рабочих столов
- Метод Connect службы удаленных рабочих столов, интерфейс Имстскакс
- Интерфейс Имстскакс службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Интерфейс Имсрдпклиент службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Интерфейс IMsRdpClient2 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Интерфейс IMsRdpClient3 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Интерфейс IMsRdpClient4 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Интерфейс IMsRdpClient5 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Интерфейс IMsRdpClient6 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Интерфейс IMsRdpClient7 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Интерфейс IMsRdpClient8 службы удаленных рабочих столов, метод Connect
- Метод Connect службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Интерфейс IMsRdpClient9 службы удаленных рабочих столов, метод Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988400"
---
# <a name="imstscaxconnect-method"></a>Метод Имстскакс:: Connect

Инициирует соединение с использованием свойств, заданных в данный момент в элементе управления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Connect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Единственным обязательным свойством является имя сервера. См. свойство [**Server**](imstscax-server.md) .

Элемент управления подключается асинхронно, поэтому возврат из вызова соединения указывает только на то, что соединение было инициировано успешно, но не завершено. Необходимо ответить на события в интерфейсе [**имстскаксевентс**](imstscaxevents-interface.md) , чтобы определить, когда элемент управления успешно подключен (или был отключен).

Этот метод возвращает **E \_ Fail** , если он вызывается, когда элемент управления уже подключен или находится в состоянии подключения.

После вызова метода **Connect** большая часть свойств элемента управления больше не может быть задана до тех пор, пока элемент управления не вернется в состояние DISCONNECTED.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиент**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**Отключение**](imstscax-disconnect.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

 





