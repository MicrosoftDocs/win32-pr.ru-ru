---
description: Содержит сведения о базовом модуле.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Структура AUX_MODULE_BASIC_INFO (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648881"
---
# <a name="aux_module_basic_info-structure"></a>\_ \_ Основная \_ информационная структура модуля AUX

Содержит сведения о базовом модуле.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**ImageBase**
</dt> <dd>

Базовый адрес модуля в адресном пространстве ядра.

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
</dt> </dl>

 

 




