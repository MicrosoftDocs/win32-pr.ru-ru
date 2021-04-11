---
title: OP_JOINPROV2_PART
description: Определение OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104134758"
---
# <a name="op_joinprov2_part-structure"></a><span data-ttu-id="15e2d-103">Структура OP_JOINPROV2_PART</span><span class="sxs-lookup"><span data-stu-id="15e2d-103">OP_JOINPROV2_PART structure</span></span>

<span data-ttu-id="15e2d-104">Содержит дополнительные сведения, используемые для настройки клиента, присоединяемого к домену.</span><span class="sxs-lookup"><span data-stu-id="15e2d-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15e2d-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a><span data-ttu-id="15e2d-106">Члены</span><span class="sxs-lookup"><span data-stu-id="15e2d-106">Members</span></span>

### <a name="dwflags"></a><span data-ttu-id="15e2d-107">dwFlags</span><span class="sxs-lookup"><span data-stu-id="15e2d-107">dwFlags</span></span>

<span data-ttu-id="15e2d-108">Необходимо задать либо ноль, либо одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="15e2d-108">Must be set to either zero or one of the following values:</span></span>

|<span data-ttu-id="15e2d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="15e2d-109">Value</span></span>|<span data-ttu-id="15e2d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="15e2d-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="15e2d-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="15e2d-111">OP_JP2_FLAG_PERSISTENTSITE (0x00000001)</span></span>|<span data-ttu-id="15e2d-112">Сайт, указанный в Лпситенаме, должен считаться постоянным сайтом для клиента.</span><span class="sxs-lookup"><span data-stu-id="15e2d-112">The site specified in lpSiteName MUST be considered the permanent site for the client.</span></span>|

### <a name="lpnetbiosname"></a><span data-ttu-id="15e2d-113">лпнетбиоснаме</span><span class="sxs-lookup"><span data-stu-id="15e2d-113">lpNetbiosName</span></span>

<span data-ttu-id="15e2d-114">Содержит NetBIOS-имя учетной записи компьютера в формате Юникода.</span><span class="sxs-lookup"><span data-stu-id="15e2d-114">Contains the Netbios name of the machine account in Unicode format.</span></span>

### <a name="lpsitename"></a><span data-ttu-id="15e2d-115">лпситенаме</span><span class="sxs-lookup"><span data-stu-id="15e2d-115">lpSiteName</span></span>

<span data-ttu-id="15e2d-116">Содержит имя Active Directory сайта, который должен использовать клиент.</span><span class="sxs-lookup"><span data-stu-id="15e2d-116">Contains the name of the Active Directory site that the client should use.</span></span>

### <a name="lpprimarydnsdomain"></a><span data-ttu-id="15e2d-117">лппримариднсдомаин</span><span class="sxs-lookup"><span data-stu-id="15e2d-117">lpPrimaryDNSDomain</span></span>

<span data-ttu-id="15e2d-118">Содержит первичное доменное имя DNS, которое должен использовать клиент.</span><span class="sxs-lookup"><span data-stu-id="15e2d-118">Contains the primary DNS domain name that the client should use.</span></span>

### <a name="dwreserved"></a><span data-ttu-id="15e2d-119">двресервед</span><span class="sxs-lookup"><span data-stu-id="15e2d-119">dwReserved</span></span>

<span data-ttu-id="15e2d-120">Зарезервировано для будущего использования и должно иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="15e2d-120">Reserved for future use and must be set to 0.</span></span>

### <a name="lpreserved"></a><span data-ttu-id="15e2d-121">lpReserved</span><span class="sxs-lookup"><span data-stu-id="15e2d-121">lpReserved</span></span>

<span data-ttu-id="15e2d-122">Зарезервировано для будущего использования и должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="15e2d-122">Reserved for future use and must be set to NULL.</span></span>

## <a name="see-also"></a><span data-ttu-id="15e2d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15e2d-123">See also</span></span>

[<span data-ttu-id="15e2d-124">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="15e2d-124">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
