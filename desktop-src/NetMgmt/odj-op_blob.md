---
title: OP_BLOB
description: Определение OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fab6df11be3bf719f787c40a41a50d948a865474
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104414048"
---
# <a name="op_blob-structure"></a><span data-ttu-id="64229-103">Структура OP_BLOB</span><span class="sxs-lookup"><span data-stu-id="64229-103">OP_BLOB structure</span></span>

<span data-ttu-id="64229-104">Содержит непрозрачный байтовый буфер.</span><span class="sxs-lookup"><span data-stu-id="64229-104">Contains an opaque byte buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="64229-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64229-105">Syntax</span></span>

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a><span data-ttu-id="64229-106">Члены</span><span class="sxs-lookup"><span data-stu-id="64229-106">Members</span></span>

### <a name="cbblob"></a><span data-ttu-id="64229-107">кбблоб</span><span class="sxs-lookup"><span data-stu-id="64229-107">cbBlob</span></span>

<span data-ttu-id="64229-108">Задает размер Пблоб в байтах.</span><span class="sxs-lookup"><span data-stu-id="64229-108">Specifies the the size of pBlob in bytes.</span></span>

### <a name="pblob"></a><span data-ttu-id="64229-109">пблоб</span><span class="sxs-lookup"><span data-stu-id="64229-109">pBlob</span></span>

<span data-ttu-id="64229-110">Указывает на буфер байтов.</span><span class="sxs-lookup"><span data-stu-id="64229-110">Points to a byte buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="64229-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64229-111">See also</span></span>

[<span data-ttu-id="64229-112">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="64229-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
