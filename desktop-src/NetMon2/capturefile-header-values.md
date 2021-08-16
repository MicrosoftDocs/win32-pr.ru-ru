---
description: Определяет структуру файла заголовка сетевой монитор.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: Структура CAPTUREFILE_HEADER_VALUES (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 29ee0ab0a9a927b3860760877457735198465b7c28789a542c040fc9e9e788a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367420"
---
# <a name="capturefile_header_values-structure"></a>\_ \_ Структура значений заголовка каптурефиле

Структура **\_ \_ значений заголовка каптурефиле** определяет структуру файла заголовка сетевой монитор.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>Члены

<dl> <dt>

**Образец**
</dt> <dd>

Уникальный идентификатор: ' ГМБУ.

</dd> <dt>

**бкдверминор**
</dt> <dd>

Двоичное, закодированное десятичное число (минор). Значение этого элемента должно быть равно нулю (0).

</dd> <dt>

**бкдвермажор**
</dt> <dd>

Двоично-кодированное десятичное число (основной). Это значение должно быть равно 2.

</dd> <dt>

**MacType**
</dt> <dd>

Тип топологии.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Время записи.

</dd> <dt>

**фраметаблеоффсет**
</dt> <dd>

Таблица индексов кадров.

</dd> <dt>

**фраметаблеленгс**
</dt> <dd>

Размер таблицы индексов кадров.

</dd> <dt>

**усердатаоффсет**
</dt> <dd>

Смещение данных пользователя.

</dd> <dt>

**усердаталенгс**
</dt> <dd>

Длина данных пользователя.

</dd> <dt>

**комментдатаоффсет**
</dt> <dd>

Смещение данных комментария.

</dd> <dt>

**комментдаталенгс**
</dt> <dd>

Длина данных комментария.

</dd> <dt>

**статистиксоффсет**
</dt> <dd>

Смещение структуры **статистики** .

</dd> <dt>

**статистиксленгс**
</dt> <dd>

Длина структуры **статистики** .

</dd> <dt>

**нетворкинфуффсет**
</dt> <dd>

Смещение к структуре **нетворкинфо** .

</dd> <dt>

**нетворкинфоленгс**
</dt> <dd>

Длина структуры **нетворкинфо** .

</dd> <dt>

**конверсатионстатсоффсет**
</dt> <dd>

Этот элемент не используется.

</dd> <dt>

**конверсатионстатсленгс**
</dt> <dd>

Этот элемент не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




