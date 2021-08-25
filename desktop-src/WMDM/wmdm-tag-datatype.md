---
title: Перечисление WMDM_TAG_DATATYPE
description: '\_ \_ Тип перечисления DATATYPE тега вмдм определяет тип данных.'
ms.assetid: 9c300814-5610-4e46-b441-e7f2fc78a47b
keywords:
- WMDM_TAG_DATATYPE перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_TAG_DATATYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd725e6d8a0e1baef8a6dfc98cb5d3056f5d67b2d7babd07c919692d96248881
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862674"
---
# <a name="wmdm_tag_datatype-enumeration"></a>\_ \_ Перечисление DATATYPE тега вмдм

Тип **перечисления \_ \_ DATATYPE тега вмдм** определяет тип данных.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWMDM_TAG_DATATYPE { 
  WMDM_TYPE_DWORD,
  WMDM_TYPE_STRING,
  WMDM_TYPE_BINARY,
  WMDM_TYPE_BOOL,
  WMDM_TYPE_QWORD,
  WMDM_TYPE_WORD,
  WMDM_TYPE_GUID,
  WMDM_TYPE_DATE
} WMDM_TAG_DATATYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDM_TYPE_DWORD"></span><span id="wmdm_type_dword"></span>**ВМДМ, \_ тип \_ DWORD**
</dt> <dd>

Задает 4-байтовое значение **DWORD** .

</dd> <dt>

<span id="WMDM_TYPE_STRING"></span><span id="wmdm_type_string"></span>**\_Строка типа \_ вмдм**
</dt> <dd>

Указывает строку в Юникоде, заканчивающуюся нулем (2 байта на символ).

</dd> <dt>

<span id="WMDM_TYPE_BINARY"></span><span id="wmdm_type_binary"></span>**\_ \_ двоичный тип вмдм**
</dt> <dd>

Указывает массив байтов.

</dd> <dt>

<span id="WMDM_TYPE_BOOL"></span><span id="wmdm_type_bool"></span>**\_bool типа \_ вмдм**
</dt> <dd>

Задает 4-байтовое логическое значение.

</dd> <dt>

<span id="WMDM_TYPE_QWORD"></span><span id="wmdm_type_qword"></span>**ВМДМ \_ тип \_ QWORD**
</dt> <dd>

Задает 8-байтовое значение **QWORD** .

</dd> <dt>

<span id="WMDM_TYPE_WORD"></span><span id="wmdm_type_word"></span>**\_слово типа \_ вмдм**
</dt> <dd>

Задает 2-байтовое значение **слова** .

</dd> <dt>

<span id="WMDM_TYPE_GUID"></span><span id="wmdm_type_guid"></span>**\_GUID типа \_ вмдм**
</dt> <dd>

Задает 128-разрядный (16-байтный) GUID.

</dd> <dt>

<span id="WMDM_TYPE_DATE"></span><span id="wmdm_type_date"></span>**ВМДМ \_ тип \_ даты**
</dt> <dd>

Указывает дату.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





