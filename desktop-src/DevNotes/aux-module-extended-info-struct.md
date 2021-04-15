---
description: Содержит расширенные сведения о модуле.
ms.assetid: 705769de-0aeb-4a28-b174-8620efa74baf
title: Структура AUX_MODULE_EXTENDED_INFO (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_EXTENDED_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 9faa706ca3603a1796d70e2f208e9b3b2e518c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648984"
---
# <a name="aux_module_extended_info-structure"></a>\_ \_ Расширенная \_ информационная структура модуля AUX

Содержит расширенные сведения о модуле.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _AUX_MODULE_EXTENDED_INFO {
  AUX_MODULE_BASIC_INFO BasicInfo;
  ULONG                 ImageSize;
  USHORT                FileNameOffset;
  UCHAR                 FullPathName[AUX_KLIB_MODULE_PATH_LEN];
} AUX_MODULE_EXTENDED_INFO, *PAUX_MODULE_EXTENDED_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**басиЦинфо**
</dt> <dd>

[**\_ \_ Базовая \_ информационная структура модуля AUX**](aux-module-basic-info-struct.md) .

</dd> <dt>

**ImageSize**
</dt> <dd>

Размер загруженного модуля в байтах.

</dd> <dt>

**филенамеоффсет**
</dt> <dd>

Смещение имени файла в буфере **фуллпаснаме** .

</dd> <dt>

**фуллпаснаме**
</dt> <dd>

Полный путь к модулю.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | Библиотека вспомогательных API Windows версии 1,0 или более поздней<br/>                          |
| Header<br/>          | <dl> <dt>AUX \_ клиб. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ауксклибкуеримодулеинформатион**](auxklibquerymoduleinformation-func.md)
</dt> <dt>

[**\_ \_ основные \_ сведения о модуле AUX**](aux-module-basic-info-struct.md)
</dt> </dl>

 

 




