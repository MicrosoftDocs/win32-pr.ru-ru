---
description: инициализирует объект системной службы для установки объекта ActiveX, если у текущего пользователя нет разрешения на установку объекта.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Интерфейс Иеаксисервице
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: f799b0b306d10e8246afbef83e4677729f6a735a52e5e4ed4954b873ec5b6201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414724"
---
# <a name="ieaxiservice-interface"></a>Интерфейс Иеаксисервице

интерфейс **иаксисервице** инициализирует объект системной службы для установки объекта ActiveX, если у текущего пользователя нет разрешения на установку объекта.

Класс [**Циеаксиинсталлерсервице**](cieaxiinstallerservice.md) реализует этот интерфейс.

Этот интерфейс не объявлен в общедоступном заголовке. Приложения должны самостоятельно определять его. Этот интерфейс описан в следующем фрагменте языка определения интерфейса (IDL), включая его IID.

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>Элементы

Интерфейс **иеаксисервице** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иеаксисервице** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иеаксисервице** содержит следующие методы.



| Метод                                        | Описание                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Очистка**](ieaxiservice-cleanup.md)       | Освобождает ресурсы, используемые интерфейсом **иеаксисервице** .<br/> |
| [**Инициализация**](ieaxiservice-initialize.md) | проверяет и скачивает объект ActiveX.<br/>                 |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista Business, Windows vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисервице определен как E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 

