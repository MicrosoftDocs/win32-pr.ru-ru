---
title: IMsRdpClientAdvancedSettings7 Нетворкконнектионтипе, свойство
description: Возвращает или задает тип сетевого подключения, используемого между клиентом и сервером. Сведения о типе сетевого подключения, передаваемые серверу, помогают серверу настроить несколько параметров на основе типа сетевого подключения.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Нетворкконнектионтипе
- Службы удаленных рабочих столов свойства Нетворкконнектионтипе, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Нетворкконнектионтипе
- Службы удаленных рабочих столов свойства Нетворкконнектионтипе, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Нетворкконнектионтипе
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e331fde1a8f7013c376b99184a90e7b3bb9f599197259b044c4d1cbd38841584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352161"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a>Свойство IMsRdpClientAdvancedSettings7:: Нетворкконнектионтипе

Возвращает или задает тип сетевого подключения, используемого между клиентом и сервером. Сведения о типе сетевого подключения, передаваемые серверу, помогают серверу настроить несколько параметров на основе типа сетевого подключения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a>Значение свойства

Тип сетевого подключения.

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Подключение к \_ Тип \_ модема** (1 (0x1))


</dt> <dd>

Модем (56 кбит/с)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Подключение к \_ Тип \_ широкополосные \_ низкая** (2 (0x2))


</dt> <dd>

Медленное широкополосное подключение (от 256 кбит/с до 2 Мбит/с)

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Подключение к \_ Тип \_ спутника** (3 (0x3))


</dt> <dd>

Вспомогательная лицензия (от 2 до 16 Мбит/с с высокой задержкой)

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Подключение к \_ Тип \_ широкополосного \_ высокого** (4 (0x4))


</dt> <dd>

Высокоскоростное широкополосное подключение (от 2 до 10 Мбит/с)

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Подключение к \_ Тип \_ WAN** (5 (0x5))


</dt> <dd>

Глобальная сеть (WAN) (от 10 Мбит/с и выше с высокой задержкой)

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Подключение к \_ Введите \_ локальную сеть** (6 (0x6))


</dt> <dd>

Локальная сеть (LAN) (10 Мбит/с или выше)

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





