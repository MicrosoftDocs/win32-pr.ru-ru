---
description: Расширяет интерфейс Итаблет.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Интерфейс ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0df1114f5808e5fd08a1a2dbe00ccfb451eaa7096c978d3f4d454e508c0a2fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717353"
---
# <a name="itablet2-interface"></a>Интерфейс ITablet2

Расширяет [**интерфейс итаблет**](itablet.md).

## <a name="members"></a>Элементы

Интерфейс **ITablet2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet2** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ITablet2** содержит следующие методы.



| Метод                                          | Описание                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**жетдевицекинд**](itablet2-getdevicekind.md) | Возвращает тип аппаратного устройства, которое представляет объект планшета, например мышь, перо или сенсорный ввод.<br/> |



 

## <a name="remarks"></a>Remarks

этот интерфейс появился в Windows Vista.

Разработчики не должны использовать этот интерфейс.

В следующем коде показано, как определяется интерфейс **ITablet2** .

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

