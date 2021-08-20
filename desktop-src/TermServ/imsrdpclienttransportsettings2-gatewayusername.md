---
title: IMsRdpClientTransportSettings2 Гатевайусернаме, свойство
description: Указывает или получает имя пользователя, предоставленное на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: eb5ed12f-e650-4abb-be20-bd5fae44e604
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайусернаме
- Службы удаленных рабочих столов свойства Гатевайусернаме, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайусернаме
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayUserName
- IMsRdpClientTransportSettings2.get_GatewayUserName
- IMsRdpClientTransportSettings2.put_GatewayUserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b5ba5c9b6d26bc2281f812674276a6f7208d31b33d33750a7a9b226aabfe4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000944"
---
# <a name="imsrdpclienttransportsettings2gatewayusername-property"></a>Свойство IMsRdpClientTransportSettings2:: Гатевайусернаме

Указывает или получает имя пользователя, предоставленное на сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayUserName(
  [in]  BSTR proxyUserName
);

HRESULT get_GatewayUserName(
  [out] BSTR *pProxyUserName
);
```



## <a name="property-value"></a>Значение свойства

Имя пользователя, которое предоставляется для подключения к серверу шлюза удаленных рабочих столов.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1)<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





