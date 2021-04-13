---
title: IMsRdpClientTransportSettings2 Гатевайенкриптедотпкукие, свойство
description: Указывает или получает зашифрованный файл cookie одноразового пароля (OTP).
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайенкриптедотпкукие
- Службы удаленных рабочих столов свойства Гатевайенкриптедотпкукие, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайенкриптедотпкукие
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5463d3d576144fc0a58b543904d6d4934b68c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535567"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a>Свойство IMsRdpClientTransportSettings2:: Гатевайенкриптедотпкукие

Указывает или получает зашифрованный файл cookie одноразового пароля (OTP).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a>Значение свойства

Указывает или получает зашифрованный файл cookie OTP.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1)<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





