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
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669098"
---
# <a name="pst_accessruleset-structure"></a>\_Структура PST акцессрулесет

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PST-файл \_ акцессруле**](pst-accessrule.md)
</dt> <dt>

[**креатесубтипе**](ipstore-createsubtype.md)
</dt> </dl>

 

 
