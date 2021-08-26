---
title: Имстскакс Сендонвиртуалчаннел, метод
description: Отправляет данные на сервер узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов) по виртуальному каналу, созданному ранее с помощью метода Креатевиртуалчаннелс.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, метод Сендонвиртуалчаннел
- Службы удаленных рабочих столов метода Сендонвиртуалчаннел, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, метод Сендонвиртуалчаннел
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03c5b84ff9cb272d5560f3b6588301a05a3e9a003db1b28f841a77b2e0618b37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125304"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>Метод Имстскакс:: Сендонвиртуалчаннел

Отправляет данные на сервер узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов) по виртуальному каналу, созданному ранее с помощью метода [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Чаннаме* \[ окне\]
</dt> <dd>

Имя виртуального канала, указанное в вызове [**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md).

</dd> <dt>

*Чандата* \[ окне\]
</dt> <dd>

Данные для отправки по виртуальному каналу в форме **BSTR** . Нет ограничений, что эти данные должны быть строками, заканчивающимися нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвратите значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Сведения об ограничениях именования виртуальных каналов см. в статье [Регистрация клиента виртуального канала](virtual-channel-client-registration.md) .

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>См. также

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

[**креатевиртуалчаннелс**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**имстскакс**](imstscax-interface.md)
</dt> </dl>

 

 





