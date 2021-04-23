---
title: ODJ_PROVISION_DATA
description: Определение ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f07d8c200103fa21afc080c60157645fe6730766
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "105719174"
---
# <a name="odj_provision_data-structure"></a><span data-ttu-id="4a2f5-103">Структура ODJ_PROVISION_DATA</span><span class="sxs-lookup"><span data-stu-id="4a2f5-103">ODJ_PROVISION_DATA structure</span></span>

<span data-ttu-id="4a2f5-104">Задает внешнюю структуру сериализации, используемую API-интерфейсами автономного присоединение к домену.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-104">Specifies the outermost serialization structure used by the offline domain join apis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a2f5-105">Syntax</span></span>

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a><span data-ttu-id="4a2f5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4a2f5-106">Members</span></span>

### <a name="ulversion"></a><span data-ttu-id="4a2f5-107">улверсион</span><span class="sxs-lookup"><span data-stu-id="4a2f5-107">ulVersion</span></span>

<span data-ttu-id="4a2f5-108">Это значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-108">This must be set to 1.</span></span>

### <a name="ulcblobs"></a><span data-ttu-id="4a2f5-109">улкблобс</span><span class="sxs-lookup"><span data-stu-id="4a2f5-109">ulcBlobs</span></span>

<span data-ttu-id="4a2f5-110">Это значение должно быть равно количеству элементов в массиве Пблобс.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-110">This must be set to the number of elements in the pBlobs array.</span></span>

### <a name="pblobs"></a><span data-ttu-id="4a2f5-111">пблобс</span><span class="sxs-lookup"><span data-stu-id="4a2f5-111">pBlobs</span></span>

<span data-ttu-id="4a2f5-112">Указывает на массив структур ODJ_BLOB.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-112">Points to an array of ODJ_BLOB structures.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a2f5-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a2f5-113">See also</span></span>

[<span data-ttu-id="4a2f5-114">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="4a2f5-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="4a2f5-115">**\_большой двоичный объект ODJ**</span><span class="sxs-lookup"><span data-stu-id="4a2f5-115">**ODJ\_BLOB**</span></span>](odj-odj_blob.md)


