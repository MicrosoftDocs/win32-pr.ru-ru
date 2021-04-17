---
title: Свойство Имстскакс Connected (Тсвиртуалчаннелс. h)
description: Возвращает состояние соединения текущего элемента управления.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Подключенное свойство службы удаленных рабочих столов
- Подключенное свойство службы удаленных рабочих столов, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, подключенное свойство
- Подключенное свойство службы удаленных рабочих столов, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, подключенное свойство
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682144"
---
# <a name="imstscaxconnected-property"></a>Свойство Имстскакс:: Connected

Возвращает состояние соединения текущего элемента управления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a>Значение свойства

Указывает состояние соединения элемента управления. Это может быть одно из следующих значений.

<dt>

0
</dt> <dd>

Элемент управления не подключен.

</dd> <dt>

1
</dt> <dd>

Элемент управления подключен.

</dd> <dt>

2
</dt> <dd>

Элемент управления устанавливает соединение.

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Предпочтительным способом определения состояния соединения элемента управления является реагирование на события соединения в [**имстскаксевентс**](imstscaxevents-interface.md).

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Тсвиртуалчаннелс. h</dt> </dl> |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>                    |



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

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

 





