---
description: устанавливает объект ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Интерфейс Иеаксисистеминсталлер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: fb462c4b4f8fc28d9d00de230dea1bbd3670c4fb6eaa962d59875b4fd9054c8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671014"
---
# <a name="ieaxisysteminstaller-interface"></a>Интерфейс Иеаксисистеминсталлер

интерфейс **иеаксисистеминсталлер** устанавливает объект ActiveX.

Этот интерфейс не объявлен в общедоступном заголовке. Приложения должны самостоятельно определять его. Этот интерфейс описан в следующем фрагменте языка определения интерфейса (IDL), включая его IID.

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>Элементы

Интерфейс **иеаксисистеминсталлер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иеаксисистеминсталлер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иеаксисистеминсталлер** содержит следующие методы.



| Метод                                                                              | Описание                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**инитиализесистеминсталлер**](ieaxisysteminstaller-initializesysteminstaller.md) | устанавливает указанный объект ActiveX.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista Business, Windows vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисистеминсталлер определен как a50ea6f8-4764-4299-b309-022b2a8b4d8d<br/>                   |



 

