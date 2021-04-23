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
# <a name="op_package-structure"></a><span data-ttu-id="c4b2e-103">Структура OP_PACKAGE</span><span class="sxs-lookup"><span data-stu-id="c4b2e-103">OP_PACKAGE structure</span></span>

<span data-ttu-id="c4b2e-104">Содержит структуру, содержащую сериализованные OP_PACKAGE_COLLECTION.</span><span class="sxs-lookup"><span data-stu-id="c4b2e-104">Contains a structure that contains a serialized OP_PACKAGE_COLLECTION.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4b2e-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c4b2e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c4b2e-106">Members</span></span>

### <a name="encryptiontype"></a><span data-ttu-id="c4b2e-107">EncryptionType</span><span class="sxs-lookup"><span data-stu-id="c4b2e-107">EncryptionType</span></span>

<span data-ttu-id="c4b2e-108">Зарезервировано для будущего использования и должно быть установлено в значение GUID_NULL.</span><span class="sxs-lookup"><span data-stu-id="c4b2e-108">Reserved for future use and MUST be set to GUID_NULL.</span></span>

### <a name="encryptioncontext"></a><span data-ttu-id="c4b2e-109">енкриптионконтекст</span><span class="sxs-lookup"><span data-stu-id="c4b2e-109">EncryptionContext</span></span>

<span data-ttu-id="c4b2e-110">Зарезервировано для будущего использования и должно иметь значение "все нули".</span><span class="sxs-lookup"><span data-stu-id="c4b2e-110">Reserved for future use and MUST be set to all zeros.</span></span>

### <a name="wrappedpartcollection"></a><span data-ttu-id="c4b2e-111">враппедпартколлектион</span><span class="sxs-lookup"><span data-stu-id="c4b2e-111">WrappedPartCollection</span></span>

<span data-ttu-id="c4b2e-112">Структура OP_BLOB, которая содержит сериализованную структуру OP_PACKAGE_COLLECTION.</span><span class="sxs-lookup"><span data-stu-id="c4b2e-112">An OP_BLOB structure that contains a serialized OP_PACKAGE_COLLECTION structure.</span></span>

### <a name="cbdecryptedpartcollection"></a><span data-ttu-id="c4b2e-113">кбдекриптедпартколлектион</span><span class="sxs-lookup"><span data-stu-id="c4b2e-113">cbDecryptedPartCollection</span></span>

<span data-ttu-id="c4b2e-114">Зарезервировано для будущего использования и должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c4b2e-114">Reserved for future use and MUST be set to zero.</span></span>

### <a name="extension"></a><span data-ttu-id="c4b2e-115">Расширение</span><span class="sxs-lookup"><span data-stu-id="c4b2e-115">Extension</span></span>

<span data-ttu-id="c4b2e-116">Зарезервировано для будущего использования и должно иметь значение "все нули".</span><span class="sxs-lookup"><span data-stu-id="c4b2e-116">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4b2e-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4b2e-117">See also</span></span>

[<span data-ttu-id="c4b2e-118">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="c4b2e-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="c4b2e-119">**\_большой двоичный объект Op**</span><span class="sxs-lookup"><span data-stu-id="c4b2e-119">**OP\_BLOB**</span></span>](odj-op_blob.md)

[<span data-ttu-id="c4b2e-120">**\_Коллекция пакетов \_ Op**</span><span class="sxs-lookup"><span data-stu-id="c4b2e-120">**OP\_PACKAGE\_COLLECTION**</span></span>](odj-op_package_collection.md)
