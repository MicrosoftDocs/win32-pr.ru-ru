---
description: Предоставляет доступ ко всем планшетам, подключенным к компьютеру.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Интерфейс Итаблетманажер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: ae4a12964ff900d8a30c0f59d2210c82007995337a2661a6fbd29a6acdfccdf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820524"
---
# <a name="itabletmanager-interface"></a>Интерфейс Итаблетманажер

Предоставляет доступ ко всем планшетам, подключенным к компьютеру.

## <a name="members"></a>Элементы

Интерфейс **итаблетманажер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Итаблетманажер** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итаблетманажер** содержит следующие методы.



| Метод                                                  | Описание                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**Подтаблица**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | Извлекает указанный объект планшета.<br/>                  |
| [**жеттаблеткаунт**](itabletmanager-gettabletcount.md) | Возвращает число планшетов, подключенных к системе.<br/> |



 

## <a name="remarks"></a>Remarks

Разработчики не должны использовать этот интерфейс.

В следующем коде показано, как реализуется интерфейс **итаблетманажер** .

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

Вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) с идентификатором класса CLSID \_ таблетманажерс, а затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель на **интерфейс итаблетманажер**. \_Идентификатор GUID ТАБЛЕТМАНАЖЕРС CLSID определяется следующим образом:

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

