---
title: Имсрдпклиенттранспортсеттингс Гатевайусажемесод, свойство
description: Указывает, когда следует использовать сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 0644c413-9ff7-42c1-a38e-e1ce546972ff
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайусажемесод
- Службы удаленных рабочих столов свойства Гатевайусажемесод, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайусажемесод
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUsageMethod
- IMsRdpClientTransportSettings.get_GatewayUsageMethod
- IMsRdpClientTransportSettings.put_GatewayUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14a177d191d3303cf44778713ebdef88db955d28ede58691bda1e9ad05aa51a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001044"
---
# <a name="imsrdpclienttransportsettingsgatewayusagemethod-property"></a>Свойство Имсрдпклиенттранспортсеттингс:: Гатевайусажемесод

Указывает, когда следует использовать сервер шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayUsageMethod(
  [in]  ULONG ulProxyMethod
);

HRESULT get_GatewayUsageMethod(
  [out] ULONG *pulProxyUsageMethod
);
```



## <a name="property-value"></a>Значение свойства

Переменная **ulong** , указывающая метод использования сервера шлюза удаленных рабочих столов. Этот параметр может принимать одно из указанных ниже значений.

<dt>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>

<span id="TSC_PROXY_MODE_NONE_DIRECT"></span><span id="tsc_proxy_mode_none_direct"></span>**Таймер TSC \_ \_Режим прокси \_ None \_ Direct** (0 (0x0))


</dt> <dd>

Не используйте сервер шлюза удаленных рабочих столов. В пользовательском интерфейсе клиента подключение к удаленному рабочему столу (RDC) флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** снят.

</dd> <dt>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>

<span id="TSC_PROXY_MODE_DIRECT"></span><span id="tsc_proxy_mode_direct"></span>**Таймер TSC \_ \_Режим прокси \_ Direct** (1 (0x1))


</dt> <dd>

Всегда используйте сервер шлюза удаленных рабочих столов. В пользовательском интерфейсе клиента RDC флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** снят.

</dd> <dt>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>

<span id="TSC_PROXY_MODE_DETECT"></span><span id="tsc_proxy_mode_detect"></span>**Таймер TSC \_ \_ \_ Обнаружение режима прокси** (2 (0x2))


</dt> <dd>

Используйте сервер шлюза удаленных рабочих столов, если не удается выполнить прямое подключение к серверу узла сеансов удаленных рабочих столов. В пользовательском интерфейсе клиента RDC установлен флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** .

</dd> <dt>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>

<span id="TSC_PROXY_MODE_DEFAULT"></span><span id="tsc_proxy_mode_default"></span>**Таймер TSC \_ \_Режим прокси \_ по умолчанию** (3 (0x3))


</dt> <dd>

Используйте параметры сервера шлюза удаленных рабочих столов по умолчанию.

</dd> <dt>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>

<span id="TSC_PROXY_MODE_NONE_DETECT"></span><span id="tsc_proxy_mode_none_detect"></span>**Таймер TSC \_ \_ \_ \_ Определение режима прокси-сервера** (4 (0x4))


</dt> <dd>

Не используйте сервер шлюза удаленных рабочих столов. В пользовательском интерфейсе клиента RDC установлен флажок не **использовать сервер шлюза удаленных рабочих столов для локальных адресов** .

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

 

 





