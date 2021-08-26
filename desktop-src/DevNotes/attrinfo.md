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
ms.openlocfilehash: 090f2ab58d8bf1eb4e379166086d31389b533712a3df23f987bba1331f990891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103734"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбформататтрибуте**](sdbformatattribute.md)
</dt> <dt>

[**сдбфрифилеаттрибутес**](sdbfreefileattributes.md)
</dt> <dt>

[**сдбжетфилеаттрибутес**](sdbgetfileattributes.md)
</dt> </dl>

 

 




