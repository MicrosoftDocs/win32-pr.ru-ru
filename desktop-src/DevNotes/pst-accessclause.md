---
description: Содержит сведения о предложении доступа для защищенного хранилища.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Структура PST_ACCESSCLAUSE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: e5933b762ac19ac188e2d7253e86482caae968abd58ecb02087c32657d250216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386184"
---
# <a name="pst_accessclause-structure"></a>\_Структура PST акцессклаусе

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Содержит сведения о предложении доступа для защищенного хранилища.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

**клаусетипе**
</dt> <dd>

Тип данных, на который указывает элемент **пбклауседата** . Дополнительные сведения см. в разделе [**типы PStore**](pstore-types.md).

</dd> <dt>

**кбклауседата**
</dt> <dd>

Размер данных, на которые указывает элемент **пбклауседата** .

</dd> <dt>

**пбклауседата**
</dt> <dd>

Указатель на данные предложения доступа.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**PST-файл \_ акцессруле**](pst-accessrule.md)
</dt> </dl>

 

 
