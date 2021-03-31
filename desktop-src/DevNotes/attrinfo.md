---
description: Содержит данные атрибутов для файла.
ms.assetid: f23f801c-826c-4269-bf96-0e01430484f4
title: Структура АТТРИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01c061330db3e97989e0700452fd4a205488a9fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895365"
---
# <a name="attrinfo-structure"></a>Структура АТТРИНФО

Содержит данные атрибутов для файла.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagATTRINFO {
  TAG   tAttrID;
  DWORD dwFlags;
  union {
    ULONGLONG ullAttr;
    DWORD     dwAttr;
    TCHAR     *lpAttr;
  };
} ATTRINFO, *PATTRINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**таттрид**
</dt> <dd>

Тип атрибута. См. раздел [типы тегов](tag-types.md).

</dd> <dt>

**dwFlags**
</dt> <dd>

Флаги для этого атрибута.



| Значение                                                                                                                                                                                                                                           | Значение                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="ATTRIBUTE_AVAILABLE"></span><span id="attribute_available"></span><dl> <dt>**Атрибут \_ ДОСТУПное**</dt> <dt>0x00000001</dt> </dl> | Атрибут доступен.<br/>                             |
| <span id="ATTRIBUTE_FAILED"></span><span id="attribute_failed"></span><dl> <dt>**Атрибут \_ Сбой**</dt> <dt>0x00000002</dt> </dl>          | Вызов завершился неудачей, так как атрибут недоступен.<br/> |



 

</dd> <dt>

**уллаттр**
</dt> <dd>

Значение **QWORD** (если тип тега — **\_ тип \_ QWORD**).

</dd> <dt>

**дваттр**
</dt> <dd>

Значение типа **DWORD** (если тип тега — **\_ тип \_ DWORD**).

</dd> <dt>

**лпаттр**
</dt> <dd>

Указатель на строку (если тип тега — **тег \_ типа \_ стрингреф**).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбформататтрибуте**](sdbformatattribute.md)
</dt> <dt>

[**сдбфрифилеаттрибутес**](sdbfreefileattributes.md)
</dt> <dt>

[**сдбжетфилеаттрибутес**](sdbgetfileattributes.md)
</dt> </dl>

 

 




