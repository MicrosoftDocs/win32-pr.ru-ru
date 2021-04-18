---
description: Вызывается, когда сертификат, возвращенный обратным вызовом Цертсторепровфиндцерт, не использовался и, следовательно, освобождается при последующем вызове Цертсторепровфиндцерт.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Функция обратного вызова Цертсторепровфрифиндцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664008"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="1b4fc-103">Функция обратного вызова Цертсторепровфрифиндцерт</span><span class="sxs-lookup"><span data-stu-id="1b4fc-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="1b4fc-104">Функция обратного вызова **цертсторепровфрифиндцерт** вызывается, когда сертификат, возвращенный обратным вызовом [**цертсторепровфиндцерт**](certstoreprovfindcert.md) , не использовался и, следовательно, освобождается при последующем вызове **цертсторепровфиндцерт**.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="1b4fc-105">Перед вызовом функции обратного вызова CLOSE все сертификаты, возвращаемые обратным вызовом [**цертсторепровфиндцерт**](certstoreprovfindcert.md) , должны быть освобождены поставщиком с помощью **цертсторепровфиндцерт** или **цертсторепровфрифиндцерт**.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4fc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b4fc-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1b4fc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b4fc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4fc-108">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b4fc-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4fc-109">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1b4fc-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b4fc-110">*пцертконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b4fc-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4fc-111">Указатель на [**\_ контекст сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="1b4fc-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="1b4fc-112">*пвсторепровфиндинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b4fc-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4fc-113">Указатель на буфер, содержащий сведения о поиске.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="1b4fc-114">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b4fc-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4fc-115">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4fc-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b4fc-116">Return value</span></span>

<span data-ttu-id="1b4fc-117">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="1b4fc-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4fc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1b4fc-118">Requirements</span></span>



| <span data-ttu-id="1b4fc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1b4fc-119">Requirement</span></span> | <span data-ttu-id="1b4fc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1b4fc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b4fc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b4fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4fc-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1b4fc-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1b4fc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b4fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4fc-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b4fc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b4fc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b4fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4fc-126">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="1b4fc-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="1b4fc-127">**цертсторепровфиндцерт**</span><span class="sxs-lookup"><span data-stu-id="1b4fc-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
