---
title: IMsRdpClientTransportSettings3 Гатевайаускукиесервераддр, свойство
description: Адрес сервера для проверки подлинности на основе файлов cookie.
ms.assetid: e00480cd-2133-42ff-8447-6c4234b56bf9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайаускукиесервераддр
- Службы удаленных рабочих столов свойства Гатевайаускукиесервераддр, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайаускукиесервераддр
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.get_GatewayAuthCookieServerAddr
- IMsRdpClientTransportSettings3.put_GatewayAuthCookieServerAddr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330a1ddb15d548988c23f8140ce848f7f68be5d1deb17fc51bd88eed23b9eec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000924"
---
# <a name="imsrdpclienttransportsettings3gatewayauthcookieserveraddr-property"></a>Свойство IMsRdpClientTransportSettings3:: Гатевайаускукиесервераддр

Адрес сервера для проверки подлинности на основе файлов cookie.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayAuthCookieServerAddr(
  [in]          BSTR bstrProxyAuthCookieServerAddr
);

HRESULT get_GatewayAuthCookieServerAddr(
  [out, retval] BSTR *pbstrProxyAuthCookieServerAddr
);
```



## <a name="property-value"></a>Значение свойства

Новый адрес сервера для проверки подлинности на основе файлов cookie.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





