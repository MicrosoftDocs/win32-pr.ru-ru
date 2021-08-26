---
description: Представляет общие сведения о кнопке на устройстве пера.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Интерфейс Итаблеткурсорбуттон
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76f5e581a4db81d9e260b388cc129d915121a69f3b360441e4220fd58aa0e623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938604"
---
# <a name="itabletcursorbutton-interface"></a>Интерфейс Итаблеткурсорбуттон

Представляет общие сведения о кнопке на устройстве пера.

## <a name="members"></a>Элементы

Интерфейс **итаблеткурсорбуттон** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Итаблеткурсорбуттон** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итаблеткурсорбуттон** содержит следующие методы.



| Метод                                         | Описание                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Извлекает уникальный идентификатор кнопки пера.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Возвращает имя кнопки пера.<br/>              |



 

## <a name="remarks"></a>Remarks

Разработчики не должны использовать этот интерфейс.

В следующем коде показано, как определяется интерфейс **итаблеткурсорбуттон** .

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Итаблеткурсорбуттон**](itabletcursorbutton.md)
</dt> </dl>

 

