---
title: ODJ_UNICODE_STRING
description: Определение ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "105719171"
---
# <a name="odj_unicode_string-structure"></a><span data-ttu-id="132f1-103">Структура ODJ_UNICODE_STRING</span><span class="sxs-lookup"><span data-stu-id="132f1-103">ODJ_UNICODE_STRING structure</span></span>

<span data-ttu-id="132f1-104">Содержит строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="132f1-104">Contains a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="132f1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="132f1-105">Syntax</span></span>

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a><span data-ttu-id="132f1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="132f1-106">Members</span></span>

### <a name="length"></a><span data-ttu-id="132f1-107">Длина</span><span class="sxs-lookup"><span data-stu-id="132f1-107">Length</span></span>

<span data-ttu-id="132f1-108">Необходимо задать значение, равное количеству байтов в буфере, содержащему строку, не включая знак завершения NULL.</span><span class="sxs-lookup"><span data-stu-id="132f1-108">Must be set to the number of bytes in Buffer containing the string, not including the NULL terminator.</span></span>

### <a name="maximumlength"></a><span data-ttu-id="132f1-109">MaximumLength</span><span class="sxs-lookup"><span data-stu-id="132f1-109">MaximumLength</span></span>

<span data-ttu-id="132f1-110">Это значение должно быть равно общему количеству байтов в буфере, не включая знак завершения NULL.</span><span class="sxs-lookup"><span data-stu-id="132f1-110">This MUST be set to the total number of bytes in Buffer, not including the NULL terminator.</span></span>

### <a name="buffer"></a><span data-ttu-id="132f1-111">Буфер</span><span class="sxs-lookup"><span data-stu-id="132f1-111">Buffer</span></span>

<span data-ttu-id="132f1-112">Должен быть строкой Юникода.</span><span class="sxs-lookup"><span data-stu-id="132f1-112">Must be a Unicode string.</span></span>

## <a name="see-also"></a><span data-ttu-id="132f1-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="132f1-113">See also</span></span>

[<span data-ttu-id="132f1-114">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="132f1-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
