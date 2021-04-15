---
title: OP_JOINPROV3_PART
description: Определение OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104414040"
---
# <a name="op_joinprov3_part-structure"></a>Структура OP_JOINPROV3_PART

Содержит дополнительные сведения, используемые для настройки клиента, присоединяемого к домену.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Члены

### <a name="rid"></a>Избежать

Необходимо задать относительный идентификатор SID учетной записи компьютера

### <a name="lpsid"></a>лпсид

Необходимо задать идентификатор безопасности учетной записи компьютера в виде строки.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)
