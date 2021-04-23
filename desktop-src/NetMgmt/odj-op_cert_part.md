---
title: OP_CERT_PART
description: Определение OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "105719169"
---
# <a name="op_cert_part-structure"></a><span data-ttu-id="518ea-103">Структура OP_CERT_PART</span><span class="sxs-lookup"><span data-stu-id="518ea-103">OP_CERT_PART structure</span></span>

<span data-ttu-id="518ea-104">Содержит сериализованные хранилища PFX и сертификатов.</span><span class="sxs-lookup"><span data-stu-id="518ea-104">Contains serialized PFX and certificate stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="518ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="518ea-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a><span data-ttu-id="518ea-106">Члены</span><span class="sxs-lookup"><span data-stu-id="518ea-106">Members</span></span>

### <a name="cpfxstores"></a><span data-ttu-id="518ea-107">кпфкссторес</span><span class="sxs-lookup"><span data-stu-id="518ea-107">cPfxStores</span></span>

<span data-ttu-id="518ea-108">Содержит количество элементов в Ппфкссторес.</span><span class="sxs-lookup"><span data-stu-id="518ea-108">Contains the number of elements in pPfxStores.</span></span>

### <a name="ppfxstores"></a><span data-ttu-id="518ea-109">ппфкссторес</span><span class="sxs-lookup"><span data-stu-id="518ea-109">pPfxStores</span></span>

<span data-ttu-id="518ea-110">Содержит массив структур OP_CERT_PFX_STORE.</span><span class="sxs-lookup"><span data-stu-id="518ea-110">Contains an array of OP_CERT_PFX_STORE structures.</span></span>

### <a name="csststores"></a><span data-ttu-id="518ea-111">ксстсторес</span><span class="sxs-lookup"><span data-stu-id="518ea-111">cSstStores</span></span>

<span data-ttu-id="518ea-112">Содержит количество элементов в Псстсторес.</span><span class="sxs-lookup"><span data-stu-id="518ea-112">Contains the number of elements in pSstStores.</span></span>

### <a name="psststores"></a><span data-ttu-id="518ea-113">псстсторес</span><span class="sxs-lookup"><span data-stu-id="518ea-113">pSstStores</span></span>

<span data-ttu-id="518ea-114">Содержит массив структур OP_CERT_SST_STORE.</span><span class="sxs-lookup"><span data-stu-id="518ea-114">Contains an array of OP_CERT_SST_STORE structures.</span></span>

### <a name="extension"></a><span data-ttu-id="518ea-115">Расширение</span><span class="sxs-lookup"><span data-stu-id="518ea-115">Extension</span></span>

<span data-ttu-id="518ea-116">Зарезервировано для будущего использования и должно содержать все нули.</span><span class="sxs-lookup"><span data-stu-id="518ea-116">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="518ea-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="518ea-117">See also</span></span>

[<span data-ttu-id="518ea-118">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="518ea-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="518ea-119">**\_ \_ хранилище PFX CERT \_**</span><span class="sxs-lookup"><span data-stu-id="518ea-119">**OP\_CERT\_PFX\_STORE**</span></span>](odj-op_cert_pfx_store.md)

[<span data-ttu-id="518ea-120">**магазин с OP \_ CERT \_ SST \_**</span><span class="sxs-lookup"><span data-stu-id="518ea-120">**OP\_CERT\_SST\_STORE**</span></span>](odj-op_cert_sst_store.md)

[<span data-ttu-id="518ea-121">**\_большой двоичный объект Op**</span><span class="sxs-lookup"><span data-stu-id="518ea-121">**OP\_BLOB**</span></span>](odj-op_blob.md)

