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
ms.openlocfilehash: 238245cdb9c0164b69434cf61f790b8f81fa3da2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491331"
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

 

 





