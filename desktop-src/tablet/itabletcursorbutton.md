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
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346865"
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



 

## <a name="remarks"></a>Комментарии

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Итаблеткурсорбуттон**](itabletcursorbutton.md)
</dt> </dl>

 

