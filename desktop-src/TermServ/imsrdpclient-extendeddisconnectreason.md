---
title: Имсрдпклиент Екстендеддисконнектреасон, свойство
description: Содержит расширенные сведения о причине отключения элемента управления.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Екстендеддисконнектреасон
- Службы удаленных рабочих столов свойства Екстендеддисконнектреасон, интерфейс IMsRdpClient10
- Службы удаленных рабочих столов интерфейса IMsRdpClient10, свойство Екстендеддисконнектреасон
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535225"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a>Свойство Имсрдпклиент:: Екстендеддисконнектреасон

Содержит расширенные сведения о причине отключения элемента управления.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a>Значение свойства

Указатель на значение [**екстендеддисконнектреасонкоде**](extendeddisconnectreasoncode.md) , указывающее причину отключения клиента.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="remarks"></a>Комментарии

Обычно этот метод вызывается в обработчике событий [**имстскаксевентс:: Ondisconnectных**](imstscaxevents-ondisconnected.md) для получения дополнительных сведений о событии отключения.

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпклиент определен как 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**Имстскаксевентс:: ondisconnectо**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





