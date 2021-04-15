---
title: ODJ_BLOB
description: Определение ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104488481"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="048d5-103">Структура ODJ_BLOB</span><span class="sxs-lookup"><span data-stu-id="048d5-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="048d5-104">Задает структуру, содержащую либо сериализованную ODJ_WIN7BLOB структуру, либо сериализованную OP_PACKAGE структуру.</span><span class="sxs-lookup"><span data-stu-id="048d5-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="048d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="048d5-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="048d5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="048d5-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="048d5-107">улоджформат</span><span class="sxs-lookup"><span data-stu-id="048d5-107">ulODJFormat</span></span>

<span data-ttu-id="048d5-108">Указывает логическую версию структуры и должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="048d5-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="048d5-109">Значение</span><span class="sxs-lookup"><span data-stu-id="048d5-109">Value</span></span>|<span data-ttu-id="048d5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="048d5-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="048d5-111">ODJ_WIN7_FORMAT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="048d5-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="048d5-112">Байты, содержащиеся в Пблоб, должны содержать сериализованную структуру ODJ_WIN7_BLOB.</span><span class="sxs-lookup"><span data-stu-id="048d5-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="048d5-113">ODJ_WIN8_FORMAT (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="048d5-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="048d5-114">Байты, содержащиеся в Пблоб, должны содержать сериализованную структуру OP_PACKAGE.</span><span class="sxs-lookup"><span data-stu-id="048d5-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="048d5-115">кбблоб</span><span class="sxs-lookup"><span data-stu-id="048d5-115">cbBlob</span></span>

<span data-ttu-id="048d5-116">Это значение должно быть равно количеству байтов в массиве Пблоб.</span><span class="sxs-lookup"><span data-stu-id="048d5-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="048d5-117">пблоб</span><span class="sxs-lookup"><span data-stu-id="048d5-117">pBlob</span></span>

<span data-ttu-id="048d5-118">Указывает на буфер байтов, содержащий сериализованную структуру, указанную в Улоджформат выше.</span><span class="sxs-lookup"><span data-stu-id="048d5-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="048d5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="048d5-119">See also</span></span>

[<span data-ttu-id="048d5-120">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="048d5-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

