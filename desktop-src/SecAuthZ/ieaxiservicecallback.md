---
description: Вызывается интерфейсом Иеаксисистеминсталлер для проверки возможности установки объекта ActiveX.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Интерфейс Иеаксисервицекаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913643"
---
# <a name="ieaxiservicecallback-interface"></a>Интерфейс Иеаксисервицекаллбакк

Интерфейс **иеаксисервицекаллбакк** вызывается интерфейсом [**иеаксисистеминсталлер**](ieaxisysteminstaller.md) , чтобы проверить возможность установки объекта ActiveX.

Класс [**Циеаксиинсталлерсервице**](cieaxiinstallerservice.md) реализует этот интерфейс.

Этот интерфейс не объявлен в общедоступном заголовке. Приложения должны самостоятельно определять его. Этот интерфейс описан в следующем фрагменте языка определения интерфейса (IDL), включая его IID.

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>Элементы

Интерфейс **иеаксисервицекаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иеаксисервицекаллбакк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иеаксисервицекаллбакк** содержит следующие методы.



| Метод                                                | Описание                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**верифифиле**](ieaxiservicecallback-verifyfile.md) | Выполняет проверки безопасности для указанного объекта ActiveX и возвращает расположение, в которое был скачан соответствующий CAB-файл.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисервицекаллбакк определен как 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



 

