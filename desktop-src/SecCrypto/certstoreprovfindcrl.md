---
description: Выполняет перечисление или поиск первого или следующего списка CRL во внешнем хранилище, удовлетворяющем заданным условиям.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Функция обратного вызова Цертсторепровфиндкрл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546306"
---
# <a name="certstoreprovfindcrl-callback-function"></a><span data-ttu-id="0af11-103">Функция обратного вызова Цертсторепровфиндкрл</span><span class="sxs-lookup"><span data-stu-id="0af11-103">CertStoreProvFindCRL callback function</span></span>

<span data-ttu-id="0af11-104">Функция обратного вызова **цертсторепровфиндкрл** перечисляет или находит первый или следующий [*список CRL*](../secgloss/c-gly.md) во внешнем [*хранилище*](../secgloss/e-gly.md) , соответствующее указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="0af11-104">The **CertStoreProvFindCRL** callback function enumerates or finds the first or next [*CRL*](../secgloss/c-gly.md) in an external [*store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af11-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0af11-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
);
```



## <a name="parameters"></a><span data-ttu-id="0af11-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0af11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0af11-107">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0af11-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af11-108">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0af11-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0af11-109">*пфиндинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0af11-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af11-110">Указатель на [**\_ хранилище сертификатов \_ Prov \_ найти \_ информационную**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) структуру, содержащую все параметры, переданные в функцию [**цертфиндкрлинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .</span><span class="sxs-lookup"><span data-stu-id="0af11-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="0af11-111">*ппревкрлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0af11-111">*pPrevCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af11-112">Указатель на структуру [**\_ контекста CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) последнего найденного списка отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0af11-112">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure of the last CRL found.</span></span> <span data-ttu-id="0af11-113">При первом вызове функции этот параметр должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0af11-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="0af11-114">При последующих вызовах ему следует задать указатель, возвращенный в параметре *пппровкрлконтекст* последнего вызова.</span><span class="sxs-lookup"><span data-stu-id="0af11-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCRLContext* parameter on the last call.</span></span> <span data-ttu-id="0af11-115">Непустой указатель , переданный в этом параметре, освобождается функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0af11-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="0af11-116">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0af11-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0af11-117">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="0af11-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="0af11-118">*ппвсторепровфиндинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0af11-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0af11-119">Указатель на указатель на буфер для возврата сведений о поставщике хранилища.</span><span class="sxs-lookup"><span data-stu-id="0af11-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="0af11-120">При необходимости обратный вызов может вернуть указатель на внутреннюю информацию поиска в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="0af11-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="0af11-121">После первого вызова этот параметр устанавливается в указатель, возвращенный предыдущим вызовом функции.</span><span class="sxs-lookup"><span data-stu-id="0af11-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="0af11-122">*пппровкрлконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0af11-122">*ppProvCrlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0af11-123">При успешном обнаружении в этом параметре возвращается указатель на найденный список отзыва сертификатов.</span><span class="sxs-lookup"><span data-stu-id="0af11-123">On a successful find, a pointer to the CRL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0af11-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0af11-124">Return value</span></span>

<span data-ttu-id="0af11-125">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="0af11-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af11-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0af11-126">Requirements</span></span>



| <span data-ttu-id="0af11-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0af11-127">Requirement</span></span> | <span data-ttu-id="0af11-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0af11-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0af11-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0af11-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0af11-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0af11-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0af11-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0af11-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0af11-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0af11-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0af11-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0af11-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af11-134">**\_ \_ \_ сведения о поиске Prov в хранилище сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="0af11-134">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="0af11-135">**цертфиндкрлинсторе**</span><span class="sxs-lookup"><span data-stu-id="0af11-135">**CertFindCRLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[<span data-ttu-id="0af11-136">**Контекст списка отзыва сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="0af11-136">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
