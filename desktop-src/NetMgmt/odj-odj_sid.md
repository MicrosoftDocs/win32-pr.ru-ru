---
title: ODJ_SID
description: Определение ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104070811"
---
# <a name="odj_sid-structure"></a><span data-ttu-id="f949a-103">Структура ODJ_SID</span><span class="sxs-lookup"><span data-stu-id="f949a-103">ODJ_SID structure</span></span>

<span data-ttu-id="f949a-104">Содержит идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="f949a-104">Contains a Security Identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="f949a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f949a-105">Syntax</span></span>

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a><span data-ttu-id="f949a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f949a-106">Members</span></span>

### <a name="revision"></a><span data-ttu-id="f949a-107">Редакция</span><span class="sxs-lookup"><span data-stu-id="f949a-107">Revision</span></span>

<span data-ttu-id="f949a-108">Необходимо задать версию идентификатора SID.</span><span class="sxs-lookup"><span data-stu-id="f949a-108">Must be set to the SID revision.</span></span>

### <a name="subauthoritycount"></a><span data-ttu-id="f949a-109">субаусоритикаунт</span><span class="sxs-lookup"><span data-stu-id="f949a-109">SubAuthorityCount</span></span>

<span data-ttu-id="f949a-110">Необходимо задать число элементов в подавторе.</span><span class="sxs-lookup"><span data-stu-id="f949a-110">Must be set to the number of elements in SubAuthority.</span></span>

### <a name="identifierauthority"></a><span data-ttu-id="f949a-111">идентифиераусорити</span><span class="sxs-lookup"><span data-stu-id="f949a-111">IdentifierAuthority</span></span>

<span data-ttu-id="f949a-112">Необходимо задать идентификатор центра безопасности.</span><span class="sxs-lookup"><span data-stu-id="f949a-112">Must be set to the SID authority identifier.</span></span>

### <a name="subauthority"></a><span data-ttu-id="f949a-113">Подавтор</span><span class="sxs-lookup"><span data-stu-id="f949a-113">SubAuthority</span></span>

<span data-ttu-id="f949a-114">Должен содержать массив вложенных центров SID.</span><span class="sxs-lookup"><span data-stu-id="f949a-114">Must contain an array of SID sub authorities.</span></span>

## <a name="see-also"></a><span data-ttu-id="f949a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f949a-115">See also</span></span>

[<span data-ttu-id="f949a-116">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="f949a-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="f949a-117">**\_ \_ центр идентификации SID \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="f949a-117">**ODJ\_SID\_IDENTIFIER\_AUTHORITY**</span></span>](odj-sid_identifier_authority.md)
