---
description: Представляет объект пера.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Интерфейс Итаблеткурсор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 83a24329b318ec2bb542a3bbb63a28d4db9fce877b99f75aa7091670825fa439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716942"
---
# <a name="itabletcursor-interface"></a>Интерфейс Итаблеткурсор

Представляет объект пера.

## <a name="members"></a>Элементы

Интерфейс **итаблеткурсор** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Итаблеткурсор** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итаблеткурсор** содержит следующие методы.



| Метод                                                 | Описание                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Кнопка**](itabletcursor-getbutton.md)           | Извлекает указанный объект кнопки из пера планшета.<br/> |
| [**жетбуттонкаунт**](itabletcursor-getbuttoncount.md) | Получает количество кнопок пера планшета.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Получает идентификатор пера.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Извлекает имя пера планшета.<br/>                    |
| [**Инверсия**](itabletcursor-isinverted.md)         | Указывает, является ли перо перевернутым.<br/>                     |



 

## <a name="remarks"></a>Remarks

Не следует использовать данный интерфейс.

В следующем коде показано, как определяется интерфейс **итаблеткурсор** .

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

