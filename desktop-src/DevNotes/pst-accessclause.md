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
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665251"
---
# <a name="pst_accessclause-structure"></a>\_Структура PST акцессклаусе

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PST-файл \_ акцессруле**](pst-accessrule.md)
</dt> </dl>

 

 
