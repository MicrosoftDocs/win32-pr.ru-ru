---
title: IMsRdpClientTransportSettings3 Гатевайенкриптедаускукиесизе, свойство
description: Размер (в символах) свойства Гатевайенкриптедаускукие.
ms.assetid: 52e24bef-5afa-4954-b639-08ea8701404a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедаускукиесизе
- Службы удаленных рабочих столов свойства Гатевайенкриптедаускукиесизе, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайенкриптедаускукиесизе
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookieSize
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookieSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e26e4d15c134bcd8a2dd5bbf74b574f38ce56627d0f7e7840547ed1d56a67a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606939"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookiesize-property"></a>Свойство IMsRdpClientTransportSettings3:: Гатевайенкриптедаускукиесизе

Размер (в символах) свойства [**гатевайенкриптедаускукие**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayEncryptedAuthCookieSize(
  [in]          ULONG ulEncryptedAuthCookieSize
);

HRESULT get_GatewayEncryptedAuthCookieSize(
  [out, retval] ULONG *ulEncryptedAuthCookieSize
);
```



## <a name="property-value"></a>Значение свойства

Значение типа **ulong** , содержащее новое значение размера.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





