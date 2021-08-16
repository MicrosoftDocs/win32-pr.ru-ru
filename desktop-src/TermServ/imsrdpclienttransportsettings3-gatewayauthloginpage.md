---
title: IMsRdpClientTransportSettings3 Гатевайауслогинпаже, свойство
description: Адрес веб-страницы входа, используемой для проверки подлинности пользователя.
ms.assetid: d7a5e0d8-353e-416d-a9e0-11ef5072f9ff
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайауслогинпаже
- Службы удаленных рабочих столов свойства Гатевайауслогинпаже, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайауслогинпаже
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.get_GatewayAuthLoginPage
- IMsRdpClientTransportSettings3.put_GatewayAuthLoginPage
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672fc929e2fccf6934a2703684e467c75fd8afb725107a73bf0f6bb311c09bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000934"
---
# <a name="imsrdpclienttransportsettings3gatewayauthloginpage-property"></a>Свойство IMsRdpClientTransportSettings3:: Гатевайауслогинпаже

Адрес веб-страницы входа, используемой для проверки подлинности пользователя.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayAuthLoginPage(
  [in]          BSTR bstrProxyAuthLoginPage
);

HRESULT get_GatewayAuthLoginPage(
  [out, retval] BSTR *pbstrProxyAuthLoginPage
);
```



## <a name="property-value"></a>Значение свойства

Новый адрес веб-страницы входа.

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

 

 





