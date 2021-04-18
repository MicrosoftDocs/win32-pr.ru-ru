---
title: OP_PACKAGE
description: Определение OP_PACKAGE IDL
ms.assetid: 065266a6-6db5-4113-bd2b-22ac6063236d
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 6220b3815ad6ff360af7255a91fc34d71125f38c
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "105719166"
---
# <a name="op_package-structure"></a>Структура OP_PACKAGE

Содержит структуру, содержащую сериализованные OP_PACKAGE_COLLECTION.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_PACKAGE
{
    GUID    EncryptionType;
    OP_BLOB EncryptionContext;
    OP_BLOB WrappedPartCollection;
    ULONG   cbDecryptedPartCollection;
    OP_BLOB Extension;
} OP_PACKAGE, *POP_PACKAGE;
```

## <a name="members"></a>Члены

### <a name="encryptiontype"></a>EncryptionType

Зарезервировано для будущего использования и должно быть установлено в значение GUID_NULL.

### <a name="encryptioncontext"></a>енкриптионконтекст

Зарезервировано для будущего использования и должно иметь значение "все нули".

### <a name="wrappedpartcollection"></a>враппедпартколлектион

Структура OP_BLOB, которая содержит сериализованную структуру OP_PACKAGE_COLLECTION.

### <a name="cbdecryptedpartcollection"></a>кбдекриптедпартколлектион

Зарезервировано для будущего использования и должно быть равно нулю.

### <a name="extension"></a>Расширение

Зарезервировано для будущего использования и должно иметь значение "все нули".

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_большой двоичный объект Op**](odj-op_blob.md)

[**\_Коллекция пакетов \_ Op**](odj-op_package_collection.md)
