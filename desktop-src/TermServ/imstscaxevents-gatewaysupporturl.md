---
title: IMsRdpClientTransportSettings2 Гатевайсуппортурл, свойство
description: Указывает или получает веб-адрес сайта, который предоставляет техническую поддержку для этого сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: e9c0f5ec-1b2f-4e09-8169-4316fd394443
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайсуппортурл
- Службы удаленных рабочих столов свойства Гатевайсуппортурл, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайсуппортурл
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewaySupportUrl
- IMsRdpClientTransportSettings2.get_GatewaySupportUrl
- IMsRdpClientTransportSettings2.put_GatewaySupportUrl
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2833962f66fb6fab2597629877c5990c9234eb5b2dfe076073bedc2ceab9fd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770694"
---
# <a name="imsrdpclienttransportsettings2gatewaysupporturl-property"></a>Свойство IMsRdpClientTransportSettings2:: Гатевайсуппортурл

Указывает или получает веб-адрес сайта, который предоставляет техническую поддержку для этого сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewaySupportUrl(
  [in]  BSTR bstrProxySupportUrl
);

HRESULT get_GatewaySupportUrl(
  [out] BSTR *pbstrProxySupportUrl
);
```



## <a name="property-value"></a>Значение свойства

Указывает или получает веб-адрес сайта, который предоставляет техническую поддержку для этого сервера шлюза удаленных рабочих столов.

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

 

 





