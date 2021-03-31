---
title: Структура MPTHREAT_INFOEX_BEHAVIOR (Мпклиент. h)
description: Содержит сведения, относящиеся к изменению поведения.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR структуры устаревшие функции среды Windows
- Функции PMPTHREAT_INFOEX_BEHAVIOR указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803532"
---
# <a name="mpthreat_infoex_behavior-structure"></a>\_ \_ Структура поведения инфоекс мпсреат

Содержит сведения, относящиеся к изменению поведения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>Члены

<dl> <dt>

**сигнатуреид**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Идентификатор подписи изменения поведения, заданный ядром во время обнаружения.

</dd> <dt>

**EngineVersion**
</dt> <dd>

Тип: **улонглонг**

</dd> <dd>

Версия модуля подсистемы.

</dd> <dt>

**асделтасигнатуреверсион**
</dt> <dd>

Тип: **улонглонг**

</dd> <dd>

Версия сигнатуры антишпионского по.

</dd> <dt>

**авделтасигнатуреверсион**
</dt> <dd>

Тип: **улонглонг**

</dd> <dd>

Версия сигнатуры Антивируса

</dd> <dt>

**хаштипе**
</dt> <dd>

Тип: **[ **\_ \_ тип хэша MP**](mp-hash-type.md)**

</dd> <dd>

Используемый тип хэша. См. раздел [**\_ \_ тип хэша MP**](mp-hash-type.md).

</dd> <dt>

**фиделитивалуе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Значение точности.

</dd> <dt>

**хашвалуе**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Хэш файла.

</dd> <dt>

**таржетфиленаме**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Путь и имя целевого файла.

</dd> <dt>

**таржетфилехаш**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Хэш целевого файла.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип ХЭША \_ MP**](mp-hash-type.md)
</dt> </dl>

 

 





