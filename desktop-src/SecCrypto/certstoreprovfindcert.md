---
description: Перечисляет или находит первый или следующий сертификат во внешнем хранилище, соответствующий указанным критериям.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Функция обратного вызова Цертсторепровфиндцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347075"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="e2c2b-103">Функция обратного вызова Цертсторепровфиндцерт</span><span class="sxs-lookup"><span data-stu-id="e2c2b-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="e2c2b-104">Функция обратного вызова **цертсторепровфиндцерт** перечисляет или находит первый или следующий сертификат во [*внешнем хранилище*](../secgloss/e-gly.md) , соответствующий указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2c2b-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="e2c2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e2c2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c2b-107">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c2b-108">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e2c2b-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2c2b-109">*пфиндинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c2b-110">Указатель на [**\_ хранилище сертификатов \_ Prov \_ найти \_ информационную**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) структуру, содержащую все параметры, переданные в функцию [**цертфиндцертификатеинсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .</span><span class="sxs-lookup"><span data-stu-id="e2c2b-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c2b-111">*ппревцертконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c2b-112">Указатель на [**\_ контекст**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) сертификата найденного сертификата.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="e2c2b-113">При первом вызове функции этот параметр должен иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="e2c2b-114">При последующих вызовах ему следует задать указатель, возвращенный в параметре *пппровцертконтекст* последнего вызова.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="e2c2b-115">Непустой указатель , переданный в этом параметре, освобождается функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c2b-116">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c2b-117">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="e2c2b-118">*ппвсторепровфиндинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c2b-119">Указатель на указатель на буфер для возврата сведений о поставщике хранилища.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="e2c2b-120">При необходимости обратный вызов может вернуть указатель на внутреннюю информацию поиска в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="e2c2b-121">После первого вызова этот параметр устанавливается в указатель, возвращенный предыдущим вызовом функции.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="e2c2b-122">*пппровцертконтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c2b-123">При успешном обнаружении в этом параметре возвращается указатель на найденный сертификат.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c2b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e2c2b-124">Return value</span></span>

<span data-ttu-id="e2c2b-125">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="e2c2b-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c2b-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e2c2b-126">Requirements</span></span>



| <span data-ttu-id="e2c2b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e2c2b-127">Requirement</span></span> | <span data-ttu-id="e2c2b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e2c2b-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2c2b-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2c2b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c2b-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e2c2b-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2c2b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c2b-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2c2b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2c2b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2c2b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c2b-134">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="e2c2b-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="e2c2b-135">**\_ \_ \_ сведения о поиске Prov в хранилище сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="e2c2b-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="e2c2b-136">**цертфиндцертификатеинсторе**</span><span class="sxs-lookup"><span data-stu-id="e2c2b-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
