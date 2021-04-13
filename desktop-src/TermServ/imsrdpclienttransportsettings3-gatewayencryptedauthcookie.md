---
title: IMsRdpClientTransportSettings3 Гатевайенкриптедаускукие, свойство
description: Зашифрованный файл cookie проверки подлинности.
ms.assetid: c9ab6667-327c-44f8-a10e-b048ea91980c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедаускукие
- Службы удаленных рабочих столов свойства Гатевайенкриптедаускукие, интерфейс IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, свойство Гатевайенкриптедаускукие
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3.GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.get_GatewayEncryptedAuthCookie
- IMsRdpClientTransportSettings3.put_GatewayEncryptedAuthCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3949d36f25f2029d7b134943b4e57d8a13db798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340685"
---
# <a name="imsrdpclienttransportsettings3gatewayencryptedauthcookie-property"></a>Свойство IMsRdpClientTransportSettings3:: Гатевайенкриптедаускукие

Зашифрованный файл cookie проверки подлинности. Размер свойства задается свойством [**гатевайенкриптедаускукиесизе**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md) .

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayEncryptedAuthCookie(
  [in]          BSTR bstrEncryptedAuthCookie
);

HRESULT get_GatewayEncryptedAuthCookie(
  [out, retval] BSTR *pbstrEncryptedAuthCookie
);
```



## <a name="property-value"></a>Значение свойства

Новый зашифрованный файл cookie проверки подлинности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**гатевайенкриптедаускукиесизе**](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)
</dt> <dt>

[**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md)
</dt> </dl>

 

 





