---
description: Описывает правило доступа к элементам, хранящимся в защищенном хранилище.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Структура PST_ACCESSRULE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 26b4df38c5e5599c13cc52a75c58ea019d786eaa971c8ac3a67a7a8c15651075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667060"
---
# <a name="pst_accessrule-structure"></a>\_Структура PST акцессруле

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Описывает правило доступа к элементам, хранящимся в защищенном хранилище.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбсизе**
</dt> <dd>

Размер этой структуры.

</dd> <dt>

**акцессмодефлагс**
</dt> <dd>

Режимы доступа, к которым относятся указанные наборы предложений доступа.



| Значение                                                                                                                                                                                                         | Значение                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> PST-файл <dt>**\_ ЧТЕНИЕ**</dt> <dt>0x0001</dt> </dl>    | Режим доступа для чтения.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> PST-файл <dt>**\_ ЗАПИСЬ**</dt> <dt>0x0002</dt> </dl> | Режим доступа для записи.<br/> |



 

</dd> <dt>

**кклаусес**
</dt> <dd>

Количество структур в массиве **ргклаусес** .

</dd> <dt>

**ргклаусес**
</dt> <dd>

Указатель на массив [**\_ акцессклаусеных структур PST**](pst-accessclause.md) .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PST-файл \_ акцессклаусе**](pst-accessclause.md)
</dt> <dt>

[**PST-файл \_ акцессрулесет**](pst-accessruleset.md)
</dt> </dl>

 

 
