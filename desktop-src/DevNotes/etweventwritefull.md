---
description: Записывает полное событие в сеанс.
title: етвевентвритефулл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWriteFull
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 1fd25931e6a58b97e052ecd7da43bd651688d2bf726d8b5ba2acd84ce820be7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653433"
---
# <a name="etweventwritefull-function"></a>Функция Етвевентвритефулл

[функция етвевентвритефулл и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут быть изменены с одного выпуска Windows на другой.]

Записывает полное событие в сеанс.

## <a name="syntax"></a>Синтаксис

```C++
ULONG
EVNTAPI
EtwEventWriteFull(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in USHORT EventProperty,
    __in_opt LPCGUID ActivityId,
    __in_opt LPCGUID RelatedActivityId,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*регхандле*
</dt> <dd>

Регхандле для поставщика.

</dd> <dt>

*EventDescriptor* 
</dt> <dd>

Дескриптор события для записи в журнал.

</dd> <dt>

*EventProperty*
</dt> <dd>

Флаг, заданный пользователем.

</dd> <dt>

*ActivityId*
</dt> <dd>

Идентификатор действия.

</dd> <dt>

*RelatedActivityId*
</dt> <dd>

Идентификатор связанного действия.

</dd> <dt>

*усердатакаунт*
</dt> <dd>

Число элементов данных пользователя.

</dd> <dt>

*UserData*
</dt> <dd>

Указатель на массив элементов данных пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Код ошибки Win32.

## <a name="remarks"></a>Remarks

функция етвевентвритефулл и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому. Чтобы обеспечить совместимость приложения, лучше использовать открытые функции.


## <a name="requirements"></a>Requirements (Требования)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Целевая платформа** | Windows |
| **Header** | нтетв. h |

## <a name="see-also"></a>См. также

<dl> <dt>

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[евентвритикс](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
