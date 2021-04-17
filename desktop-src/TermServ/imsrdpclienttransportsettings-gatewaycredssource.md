---
title: Имсрдпклиенттранспортсеттингс Гатевайкредссаурце, свойство
description: Указывает или получает метод проверки подлинности шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайкредссаурце
- Службы удаленных рабочих столов свойства Гатевайкредссаурце, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайкредссаурце
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415049"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a>Свойство Имсрдпклиенттранспортсеттингс:: Гатевайкредссаурце

Указывает или получает метод проверки подлинности шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a>Значение свойства

Переменная **ulong** , указывающая метод проверки подлинности шлюза удаленных рабочих столов. Этот параметр может принимать одно из указанных ниже значений.

<dt>

\_Усерпасс режима прокси-сервера TSC \_ \_ \_ (0)
</dt> <dd>

Используйте пароль (NTLM) в качестве метода проверки подлинности для шлюза удаленных рабочих столов.

</dd> <dt>

\_Смарт-прокси режим учетных записи \_ \_ \_ (1)
</dt> <dd>

Используйте смарт-карту в качестве метода проверки подлинности для шлюза удаленных рабочих столов.

</dd> <dt>

В \_ режиме прокси-сервера TSC \_ \_ \_ ANY (4)
</dt> <dd>

Используйте любой метод проверки подлинности для шлюза удаленных рабочих столов.

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





