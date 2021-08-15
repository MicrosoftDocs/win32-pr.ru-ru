---
title: Структура MPFASTPATH_DATA (Мпклиент. h)
description: Уведомление об обновлении Фастпас.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA структуры устаревшие функции среды Windows
- функции PMPFASTPATH_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556154"
---
# <a name="mpfastpath_data-structure"></a>\_Структура данных мпфастпас

Уведомление об обновлении Фастпас.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**сигнатуретипе**
</dt> <dd>

Тип: **[ **\_ \_ тип подписи пакета управления**](mp-signature-type.md)**

</dd> <dd>

Тип подписи.

</dd> <dt>

**фастпассигнатуретипе**
</dt> <dd>

Тип: **[ **\_ \_ тип MP фастпас**](mp-fastpath-type.md)**

</dd> <dd>

Тип подписи Фастпас.

</dd> <dt>

**фастпассигнатуреверсион**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Версия сигнатуры Фастпас (необязательно).

</dd> <dt>

**компилатионтиместамп**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Отметка времени компиляции (UTC).

</dd> <dt>

**PersistenceType**
</dt> <dd>

Тип: **[ **\_ \_ \_ тип ограничения сохраняемости MP**](mp-persistence-limit-type.md)**

</dd> <dd>

Тип сохраняемости (необязательный).

</dd> <dt>

**персистенцевалуе**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Значение сохраняемости (необязательно).

</dd> <dt>

**персистенцепас**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Путь сохраняемости (необязательно).

</dd> <dt>

**Причина**
</dt> <dd>

Тип: **[ **\_ \_ Причина удаления пакета управления**](mp-removal-reason.md)**

</dd> <dd>

Причина удаления подписи.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_тип фастпас пакета управления \_**](mp-fastpath-type.md)
</dt> <dt>

[**\_тип ограничения сохраняемости пакета управления \_ \_**](mp-persistence-limit-type.md)
</dt> <dt>

[**\_тип подписи пакета управления \_**](mp-signature-type.md)
</dt> </dl>

 

 





