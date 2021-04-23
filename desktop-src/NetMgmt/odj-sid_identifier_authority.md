---
title: SID_IDENTIFIER_AUTHORITY
description: Определение SID_IDENTIFIER_AUTHORITY IDL
ms.assetid: 88fe41f4-1c67-4290-ac21-fd43ff12d825
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d9a80ed0717a279f39ac7a105a95807911232c82
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104134759"
---
# <a name="sid_identifier_authority-structure"></a><span data-ttu-id="98b2b-103">Структура SID_IDENTIFIER_AUTHORITY</span><span class="sxs-lookup"><span data-stu-id="98b2b-103">SID_IDENTIFIER_AUTHORITY structure</span></span>

<span data-ttu-id="98b2b-104">Содержит центр идентификации SID.</span><span class="sxs-lookup"><span data-stu-id="98b2b-104">Contains a SID identifier authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98b2b-105">Syntax</span></span>

```C++
typedef struct _SID_IDENTIFIER_AUTHORITY
{
    UCHAR Value[6];
} SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;
```

## <a name="members"></a><span data-ttu-id="98b2b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="98b2b-106">Members</span></span>

### <a name="value"></a><span data-ttu-id="98b2b-107">Значение</span><span class="sxs-lookup"><span data-stu-id="98b2b-107">Value</span></span>

<span data-ttu-id="98b2b-108">Необходимо задать шесть байтов центра идентификации SID.</span><span class="sxs-lookup"><span data-stu-id="98b2b-108">Must be set to the six bytes of the SID identifier authority.</span></span>

## <a name="see-also"></a><span data-ttu-id="98b2b-109">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98b2b-109">See also</span></span>

[<span data-ttu-id="98b2b-110">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="98b2b-110">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)