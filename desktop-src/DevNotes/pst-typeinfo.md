---
description: Описывает тип или подтип.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Структура PST_TYPEINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 8f196b455ce598ca4ad793c18b06508c24ce15068479535b05bae398daad5dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571794"
---
# <a name="pst_typeinfo-structure"></a>\_Структура файла подструктуры PST

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Описывает тип или подтип.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

**сздисплайнаме**
</dt> <dd>

Указатель на строку расширенных символов, представляющую отображаемое имя типа.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**креатесубтипе**](ipstore-createsubtype.md)
</dt> <dt>

[**CreateType**](ipstore-createtype.md)
</dt> <dt>

[**жетсубтипеинфо**](ipstore-getsubtypeinfo.md)
</dt> <dt>

[**GetTypeInfo**](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
