---
description: Дополнительные сведения о функции Етвевентврите
title: етвевентврите
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: b8e06c2a0922038e37766f44c0b9fcd7c85bbb7fd4fa4bd0841192be9e4e9087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162105"
---
# <a name="etweventwrite-function"></a>Функция Етвевентврите

[функция етвевентврите и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут быть изменены с одного выпуска Windows на другой.]

Записывает базовое событие в сеанс.

## <a name="syntax"></a>Синтаксис

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
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

функция етвевентврите и возвращаемые ею структуры являются внутренними по отношению к операционной системе и могут изменяться от одного выпуска Windows к другому. Чтобы обеспечить совместимость приложения, лучше использовать открытые функции.

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
