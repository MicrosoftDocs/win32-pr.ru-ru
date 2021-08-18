---
description: Определяет методы, обрабатывающие события интерфейса Итаблет.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Интерфейс Итаблетевентсинк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: a1a773f7b4e08a718c419de2d51c0ff3bd9bba551267188b12889b9ec99d4ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716463"
---
# <a name="itableteventsink-interface"></a>Интерфейс Итаблетевентсинк

Определяет методы, обрабатывающие события [**интерфейса итаблет**](itablet.md) .

## <a name="members"></a>Элементы

Интерфейс **итаблетевентсинк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Итаблетевентсинк** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **итаблетевентсинк** содержит следующие методы.



| Метод                                                        | Описание                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**контексткреате**](itableteventsink-contextcreate.md)       | Происходит при создании нового контекста планшета.<br/>                                          |
| [**контекстдестрой**](itableteventsink-contextdestroy.md)     | Происходит при уничтожении контекста планшета.<br/>                                      |
| [**курсордовн**](itableteventsink-cursordown.md)             | Происходит, когда подсказка пера обращается к поверхности планшета в дигитайзере.<br/>                    |
| [**курсоринранже**](itableteventsink-cursorinrange.md)       | Происходит, когда перо попадает в диапазон обнаружения дигитайзера.<br/>                 |
| [**курсормове**](itableteventsink-cursormove.md)             | Происходит при наведении курсора мыши на планшетном дигитайзере.<br/>                               |
| [**курсорнев**](itableteventsink-cursornew.md)               | Происходит при добавлении нового пера в систему.<br/>                                      |
| [**курсораутофранже**](itableteventsink-cursoroutofrange.md) | Происходит, когда перо покидает диапазон физического обнаружения (близость) планшета.<br/> |
| [**курсоруп**](itableteventsink-cursorup.md)                 | Происходит, когда пользователь порождает перо из поверхности планшета дигитайзера.<br/>         |
| [**Пакеты**](itableteventsink-packets.md)                   | Происходит при перемещении пера на дигитайзер.<br/>                                    |
| [**системевент**](itableteventsink-systemevent.md)           | Происходит при наличии системного события.<br/>                                              |



 

## <a name="remarks"></a>Remarks

Разработчики не должны использовать этот интерфейс.

В следующем коде показано, как определяется интерфейс **итаблетевентсинк** .

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

