---
description: Выполняет перечисление или поиск первого или следующего списка доверия (CTL) во внешнем хранилище, соответствующем указанным критериям.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Функция обратного вызова Цертсторепровфиндктл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664009"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="0fb75-103">Функция обратного вызова Цертсторепровфиндктл</span><span class="sxs-lookup"><span data-stu-id="0fb75-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="0fb75-104">Функция обратного вызова **цертсторепровфиндктл** перечисляет или находит первый или следующий [*список CTL*](../secgloss/c-gly.md) во [*внешнем хранилище*](../secgloss/e-gly.md) , соответствующий указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="0fb75-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb75-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fb75-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="0fb75-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fb75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb75-107">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb75-108">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0fb75-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fb75-109">*пфиндинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb75-110">Указатель на [**\_ хранилище сертификатов \_ Prov \_ найти \_ информационную**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) структуру, содержащую все параметры, переданные в [**цертфиндктлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="0fb75-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="0fb75-111">.</span><span class="sxs-lookup"><span data-stu-id="0fb75-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="0fb75-112">*ппревктлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb75-113">Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) для последнего найденного списка доверия.</span><span class="sxs-lookup"><span data-stu-id="0fb75-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="0fb75-114">При первом вызове функции этот параметр должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0fb75-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="0fb75-115">При последующих вызовах ему следует задать указатель, возвращенный в параметре *пппровктлконтекст* последнего вызова.</span><span class="sxs-lookup"><span data-stu-id="0fb75-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="0fb75-116">Непустой указатель , переданный в этом параметре, освобождается функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0fb75-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0fb75-117">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb75-118">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="0fb75-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="0fb75-119">*ппвсторепровфиндинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb75-120">Указатель на указатель на буфер для возврата сведений о поставщике хранилища.</span><span class="sxs-lookup"><span data-stu-id="0fb75-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="0fb75-121">При необходимости обратный вызов может вернуть указатель на внутреннюю информацию поиска в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="0fb75-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="0fb75-122">После первого вызова этот параметр устанавливается в указатель, возвращенный предыдущим вызовом функции.</span><span class="sxs-lookup"><span data-stu-id="0fb75-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="0fb75-123">*пппровктлконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fb75-124">При успешном обнаружении в этом параметре возвращается указатель на найденный список доверия.</span><span class="sxs-lookup"><span data-stu-id="0fb75-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb75-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fb75-125">Return value</span></span>

<span data-ttu-id="0fb75-126">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="0fb75-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb75-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0fb75-127">Requirements</span></span>



| <span data-ttu-id="0fb75-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0fb75-128">Requirement</span></span> | <span data-ttu-id="0fb75-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0fb75-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fb75-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0fb75-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb75-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0fb75-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0fb75-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb75-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0fb75-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0fb75-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fb75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb75-135">**\_ \_ \_ сведения о поиске Prov в хранилище сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="0fb75-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="0fb75-136">**цертфиндктлинсторе**</span><span class="sxs-lookup"><span data-stu-id="0fb75-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="0fb75-137">**\_контекст CTL**</span><span class="sxs-lookup"><span data-stu-id="0fb75-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
