---
description: Вызывается, когда сертификат, возвращенный обратным вызовом Цертсторепровфиндкрл, не использовался и, следовательно, освобождается при последующем вызове Цертсторепровфиндкрл.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Функция обратного вызова Цертсторепровфрифиндкрл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911787"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="93657-103">Функция обратного вызова Цертсторепровфрифиндкрл</span><span class="sxs-lookup"><span data-stu-id="93657-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="93657-104">Функция обратного вызова **цертсторепровфрифиндкрл** вызывается, когда сертификат, возвращенный обратным вызовом [**цертсторепровфиндкрл**](certstoreprovfindcrl.md) , не использовался и, следовательно, освобождается при последующем вызове **цертсторепровфиндкрл**.</span><span class="sxs-lookup"><span data-stu-id="93657-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="93657-105">Перед вызовом функции обратного вызова CLOSE все сертификаты, возвращаемые обратным вызовом [**цертсторепровфиндкрл**](certstoreprovfindcrl.md) , должны быть освобождены поставщиком с помощью **цертсторепровфиндкрл** или **цертсторепровфрифиндкрл**.</span><span class="sxs-lookup"><span data-stu-id="93657-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="93657-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93657-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="93657-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="93657-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93657-108">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93657-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93657-109">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="93657-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="93657-110">*пкрлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93657-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93657-111">Указатель на [**\_ контекст списка отзыва сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="93657-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="93657-112">*пвсторепровфиндинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93657-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93657-113">Указатель на буфер, содержащий сведения о поиске.</span><span class="sxs-lookup"><span data-stu-id="93657-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="93657-114">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93657-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93657-115">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="93657-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93657-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93657-116">Return value</span></span>

<span data-ttu-id="93657-117">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="93657-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="93657-118">Требования</span><span class="sxs-lookup"><span data-stu-id="93657-118">Requirements</span></span>



| <span data-ttu-id="93657-119">Требование</span><span class="sxs-lookup"><span data-stu-id="93657-119">Requirement</span></span> | <span data-ttu-id="93657-120">Значение</span><span class="sxs-lookup"><span data-stu-id="93657-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93657-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93657-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93657-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93657-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="93657-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93657-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93657-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93657-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93657-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93657-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93657-126">**цертсторепровфиндкрл**</span><span class="sxs-lookup"><span data-stu-id="93657-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="93657-127">**Контекст списка отзыва сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="93657-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
