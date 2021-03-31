---
title: IMsRdpClientAdvancedSettings6 AuthenticationType, свойство
description: Указывает тип проверки подлинности, используемый для этого соединения.
ms.assetid: A6DAAE0A-5045-4C2C-B065-AB5BFB39F955
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства AuthenticationType
- Службы удаленных рабочих столов свойства AuthenticationType, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, Свойство AuthenticationType
- Службы удаленных рабочих столов свойства AuthenticationType, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, Свойство AuthenticationType
- Службы удаленных рабочих столов свойства AuthenticationType, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, Свойство AuthenticationType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.AuthenticationType
- IMsRdpClientAdvancedSettings6.get_AuthenticationType
- IMsRdpClientAdvancedSettings7.AuthenticationType
- IMsRdpClientAdvancedSettings7.get_AuthenticationType
- IMsRdpClientAdvancedSettings8.AuthenticationType
- IMsRdpClientAdvancedSettings8.get_AuthenticationType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c59239570538b690866e499ee942b6635055c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135906"
---
# <a name="imsrdpclientadvancedsettings6authenticationtype-property"></a>Свойство IMsRdpClientAdvancedSettings6:: AuthenticationType

Указывает тип проверки подлинности, используемый для этого соединения.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_AuthenticationType(
  [out] UINT *puiAuthType
);
```



## <a name="property-value"></a>Значение свойства

Получает значение, указывающее тип проверки подлинности, используемый для этого соединения. Это может быть одно из следующих значений.

<dt>

0
</dt> <dd>

Проверка подлинности не используется.

</dd> <dt>

1
</dt> <dd>

Используется проверка подлинности с помощью сертификата.

</dd> <dt>

2
</dt> <dd>

Используется проверка подлинности Kerberos.

</dd> <dt>

3
</dt> <dd>

Используются как сертификат, так и проверка подлинности Kerberos.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





