---
title: OP_PACKAGE_PART_COLLECTION
description: Определение OP_PACKAGE_PART_COLLECTION IDL
ms.assetid: a7abf011-0335-4869-b4d9-144b2f392241
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8eb61397045a382fe5933025a4eeda2f563e838
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104070809"
---
# <a name="op_package_part_collection-structure"></a><span data-ttu-id="8fbc3-103">Структура OP_PACKAGE_PART_COLLECTION</span><span class="sxs-lookup"><span data-stu-id="8fbc3-103">OP_PACKAGE_PART_COLLECTION structure</span></span>

<span data-ttu-id="8fbc3-104">Задает структуру, содержащую массив структур OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-104">Specifies a structure that contains an array of OP_PACKAGE_PART structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbc3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fbc3-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART_COLLECTION
{
    ULONG                                 cParts;
    [size_is(cParts)]   POP_PACKAGE_PART  pParts;
    OP_BLOB                               Extension;
} OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;
```

## <a name="members"></a><span data-ttu-id="8fbc3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="8fbc3-106">Members</span></span>

### <a name="cparts"></a><span data-ttu-id="8fbc3-107">кпартс</span><span class="sxs-lookup"><span data-stu-id="8fbc3-107">cParts</span></span>

<span data-ttu-id="8fbc3-108">Содержит количество элементов в Ппартс.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-108">Contains the number of elements in pParts.</span></span>

### <a name="pparts"></a><span data-ttu-id="8fbc3-109">ппартс</span><span class="sxs-lookup"><span data-stu-id="8fbc3-109">pParts</span></span>

<span data-ttu-id="8fbc3-110">Содержит массив структур OP_PACKAGE_PART.</span><span class="sxs-lookup"><span data-stu-id="8fbc3-110">Contains an array of OP_PACKAGE_PART structures.</span></span>

### <a name="extension"></a><span data-ttu-id="8fbc3-111">Расширение</span><span class="sxs-lookup"><span data-stu-id="8fbc3-111">Extension</span></span>

<span data-ttu-id="8fbc3-112">Зарезервировано для будущего использования и должно иметь значение "все нули".</span><span class="sxs-lookup"><span data-stu-id="8fbc3-112">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fbc3-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fbc3-113">See also</span></span>

[<span data-ttu-id="8fbc3-114">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="8fbc3-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="8fbc3-115">**\_часть пакета \_ Op**</span><span class="sxs-lookup"><span data-stu-id="8fbc3-115">**OP\_PACKAGE\_PART**</span></span>](odj-op_package_part.md)

[<span data-ttu-id="8fbc3-116">**\_большой двоичный объект Op**</span><span class="sxs-lookup"><span data-stu-id="8fbc3-116">**OP\_BLOB**</span></span>](odj-op_blob.md)

