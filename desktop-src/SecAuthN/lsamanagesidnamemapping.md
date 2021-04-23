---
UID: ''
title: Функция Лсаманажесиднамемаппинг
description: Добавляет или удаляет сопоставления SID и имен из набора сопоставлений, зарегистрированного в службе LSA Lookup.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "104336620"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="4ef2f-103">Функция Лсаманажесиднамемаппинг</span><span class="sxs-lookup"><span data-stu-id="4ef2f-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="4ef2f-104">Описание</span><span class="sxs-lookup"><span data-stu-id="4ef2f-104">Description</span></span>

<span data-ttu-id="4ef2f-105">Функция **лсаманажесиднамемаппинг** добавляет или УДАЛЯЕТ сопоставления SID/имени из набора сопоставлений, зарегистрированного в службе LSA Lookup.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="4ef2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ef2f-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="4ef2f-107">OpType [in]</span><span class="sxs-lookup"><span data-stu-id="4ef2f-107">OpType [in]</span></span>

<span data-ttu-id="4ef2f-108">Указывает, вызывается ли эта функция для добавления или удаления сопоставления SID и имени.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="4ef2f-109">Опинпут [in]</span><span class="sxs-lookup"><span data-stu-id="4ef2f-109">OpInput [in]</span></span>

<span data-ttu-id="4ef2f-110">Указывает значения домена, учетной записи и идентификатора безопасности, используемые во время этой операции.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="4ef2f-111">В этой структуре также можно задать дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="4ef2f-112">Опаутпут [out]</span><span class="sxs-lookup"><span data-stu-id="4ef2f-112">OpOutput [out]</span></span>

<span data-ttu-id="4ef2f-113">Содержит значение [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) , показывающее успешность операции или сбой.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="4ef2f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4ef2f-114">Value</span></span> | <span data-ttu-id="4ef2f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4ef2f-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="4ef2f-116">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-116">**Success**</span></span> | <span data-ttu-id="4ef2f-117">Операция завершена без ошибок.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="4ef2f-118">**нонмаппинжеррор**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-118">**NonMappingError**</span></span> | <span data-ttu-id="4ef2f-119">Произошла ошибка, не связанная с сопоставлением имени SID.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="4ef2f-120">**намеколлисион**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-120">**NameCollision**</span></span> | <span data-ttu-id="4ef2f-121">Сбой операции из-за конфликта имен.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="4ef2f-122">**сидколлисион**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-122">**SidCollision**</span></span> | <span data-ttu-id="4ef2f-123">Сбой операции из-за конфликта SID.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="4ef2f-124">**DomainNotFound**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-124">**DomainNotFound**</span></span> | <span data-ttu-id="4ef2f-125">Соответствующий домен не найден.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="4ef2f-126">**домаинсидпрефиксмисматч**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="4ef2f-127">Указанный идентификатор безопасности не имеет правильного префикса домена.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="4ef2f-128">**маппингнотфаунд**</span><span class="sxs-lookup"><span data-stu-id="4ef2f-128">**MappingNotFound**</span></span> | <span data-ttu-id="4ef2f-129">Сопоставление не найдено в кэше.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="4ef2f-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ef2f-130">Returns</span></span>

<span data-ttu-id="4ef2f-131">Если сопоставление успешно вставлено, возвращаемое значение будет STATUS_SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="4ef2f-132">В противном случае, если функция завершилась ошибкой из-за конфликта SID или имени, будет возвращена STATUS_INVALID_PARAMETER ошибка.</span><span class="sxs-lookup"><span data-stu-id="4ef2f-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ef2f-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ef2f-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="4ef2f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ef2f-134">See also</span></span>
