---
description: Реализует интерфейсы Иаксисервице и Иеаксисервицекаллбакк.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Объект Циеаксиинсталлерсервице
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991194"
---
# <a name="cieaxiinstallerservice-object"></a>Объект Циеаксиинсталлерсервице

Объект **Циеаксиинсталлерсервице** реализует интерфейсы [**иаксисервице**](ieaxiservice.md) и [**иеаксисервицекаллбакк**](ieaxiservicecallback.md) .

Этот объект не объявлен в общедоступном заголовке. Приложения должны самостоятельно определять его. Этот объект описан в следующем фрагменте языка определения интерфейса (IDL), включая его CLSID.

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иаксисервице**](ieaxiservice.md)
</dt> <dt>

[**иеаксисервицекаллбакк**](ieaxiservicecallback.md)
</dt> </dl>

 

 




