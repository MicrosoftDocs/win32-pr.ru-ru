---
description: Структура КАПТУРЕФИЛТЕР содержит данные фильтра записи.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Структура КАПТУРЕФИЛТЕР (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663648"
---
# <a name="capturefilter-structure"></a>Структура КАПТУРЕФИЛТЕР

Структура **каптурефилтер** содержит данные фильтра записи.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>Члены

<dl> <dt>

**филтерфлагс**
</dt> <dd>

Флаги, описывающие содержимое фильтра записи.



| Значение                                                                                                                                                                                                                                                                                                   | Значение                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**Каптурефилтер \_ ФЛАГи \_ включают \_ все \_ SAPS**</dt> <dt>0x0001</dt> </dl>       | Включает все SAPs в качестве допустимых кадров.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**Каптурефилтер \_ ФЛАГи \_ включают \_ все \_ ETYPE**</dt> <dt>0x0002</dt> </dl> | Включите все ETYPE в качестве допустимых кадров.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**Каптурефилтер \_ ПОМЕЧАЕТ \_ \_ только локальные**</dt> <dt>0x0008</dt> </dl>                          | Без режима P-Mode<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**Каптурефилтер \_ ФЛАГи \_ сохраняют \_ необработанные**</dt> <dt>0x0020</dt> </dl>                                | Не используйте кадры MAC SMT и Token Ring.<br/>      |



 

</dd> <dt>

**лпсаптабле**
</dt> <dd>

Указатель на массив значений SAP. Этот элемент указывает значения SAP, допустимые для передачи в драйвер. Если \_ Флаги каптурефилтер \_ включают \_ все \_ SAPS, это становится списком исключений (включая все SAPS, Кроме этих).

</dd> <dt>

**лпетипетабле**
</dt> <dd>

Указатель на массив значений etype. Это означает, что значения ETYPE, допустимые для передачи в драйвер. Если \_ установлены флаги каптурефилтер \_ \_ \_ , то он становится списком исключений (включая все типы ETYPE, Кроме этих).

</dd> <dt>

**нсапс**
</dt> <dd>

Число SAPs в таблице SAP.

</dd> <dt>

**нетипес**
</dt> <dd>

Число ETYPE в таблице etype.

</dd> <dt>

**аддресстабле**
</dt> <dd>

Имя таблицы адресов.

</dd> <dt>

**FilterExpression**
</dt> <dd>

Структура выражения. Он содержит часть фильтра записи, соответствующую шаблону.

</dd> <dt>

**Триггер**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**нфрамебитестокопи**
</dt> <dd>

Если этот элемент не равен 0, то он указывает, сколько байтов следует удерживать для каждого полученного кадра. Если это 0, сохраните весь кадр целиком.

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Сочетание флагов, значений и выражений определяет, какие кадры будут переданы драйвером, использующим эти данные структуры. Дополнительные сведения о реализации структуры **каптурефилтер** см. в разделе [фильтры записи](capture-filters.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[аддресстабле](addresstable.md)
</dt> <dt>

[аддресспаир](addresspair.md)
</dt> <dt>

[ВЫРАЖЕНИЕ](expression.md)
</dt> <dt>

[андексп](andexp.md)
</dt> <dt>

[паттернматч](patternmatch.md)
</dt> </dl>

 

 




