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
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913300"
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



 

## <a name="remarks"></a>Комментарии

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
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

