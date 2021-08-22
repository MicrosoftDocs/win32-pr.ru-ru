---
description: Определяет набор правил доступа для данных защищенного хранилища.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Структура PST_ACCESSRULESET (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 9695af01c6f0ffb33fe20a112659444011ad9c18812b8d2fd885641635c6b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666981"
---
# <a name="pst_accessruleset-structure"></a>\_Структура PST акцессрулесет

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Определяет набор правил доступа для данных защищенного хранилища.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

**крулес**
</dt> <dd>

Число правил в массиве **ргрулес** .

</dd> <dt>

**ргрулес**
</dt> <dd>

Указатель на массив [**\_ акцессруленых структур PST**](pst-accessrule.md) .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PST-файл \_ акцессруле**](pst-accessrule.md)
</dt> <dt>

[**креатесубтипе**](ipstore-createsubtype.md)
</dt> </dl>

 

 
