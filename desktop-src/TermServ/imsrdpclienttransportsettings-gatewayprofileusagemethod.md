---
title: Имсрдпклиенттранспортсеттингс Гатевайпрофилеусажемесод, свойство
description: Указывает, следует ли использовать параметры шлюза удаленный рабочий стол по умолчанию (шлюз удаленных рабочих столов).
ms.assetid: ce774790-31ad-40ba-ba8f-e81b0dbda175
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайпрофилеусажемесод
- Службы удаленных рабочих столов свойства Гатевайпрофилеусажемесод, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайпрофилеусажемесод
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.get_GatewayProfileUsageMethod
- IMsRdpClientTransportSettings.put_GatewayProfileUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3386e6a38c99539aebb84280dc8250b2d779f5d81229763d2d926ae499e144e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138627"
---
# <a name="imsrdpclienttransportsettingsgatewayprofileusagemethod-property"></a>Свойство Имсрдпклиенттранспортсеттингс:: Гатевайпрофилеусажемесод

Указывает, следует ли использовать параметры шлюза удаленный рабочий стол по умолчанию (шлюз удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayProfileUsageMethod(
  [in]  ULONG ulProxyProfileMethod
);

HRESULT get_GatewayProfileUsageMethod(
  [out] ULONG *pulProxyProfileUsageMethod
);
```



## <a name="property-value"></a>Значение свойства

Метод использования профиля шлюза удаленных рабочих столов. Этот параметр может принимать одно из указанных ниже значений.

<dt>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>

<span id="TSC_PROXY_PROFILE_MODE_DEFAULT"></span><span id="tsc_proxy_profile_mode_default"></span>**Таймер TSC \_ \_Режим профиля \_ прокси \_ по умолчанию** (0 (0x0))


</dt> <dd>

Используйте режим профиля по умолчанию, указанный администратором.

</dd> <dt>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>

<span id="TSC_PROXY_PROFILE_MODE_EXPLICIT"></span><span id="tsc_proxy_profile_mode_explicit"></span>**Таймер TSC \_ \_ \_ \_ Явный режим профиля прокси-сервера** (1 (0x1))


</dt> <dd>

Используйте явные параметры, указанные пользователем.

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

 

 





