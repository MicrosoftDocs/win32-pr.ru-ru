---
description: Вызывается, когда сертификат, возвращенный обратным вызовом Цертсторепровфиндктл, не использовался и, следовательно, освобождается при последующем вызове Цертсторепровфиндктл.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Функция обратного вызова Цертсторепровфрифиндктл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683293"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="7facf-103">Функция обратного вызова Цертсторепровфрифиндктл</span><span class="sxs-lookup"><span data-stu-id="7facf-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="7facf-104">Функция обратного вызова **цертсторепровфрифиндктл** вызывается, когда сертификат, возвращенный обратным вызовом [**цертсторепровфиндктл**](certstoreprovfindctl.md) , не использовался и, следовательно, освобождается при последующем вызове **цертсторепровфиндктл**.</span><span class="sxs-lookup"><span data-stu-id="7facf-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="7facf-105">Перед вызовом функции обратного вызова CLOSE все сертификаты, возвращаемые обратным вызовом [**цертсторепровфиндктл**](certstoreprovfindctl.md) , должны быть освобождены поставщиком с помощью **цертсторепровфиндктл** или **цертсторепровфрифиндктл**.</span><span class="sxs-lookup"><span data-stu-id="7facf-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7facf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7facf-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7facf-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7facf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7facf-108">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7facf-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7facf-109">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7facf-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7facf-110">*пктлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7facf-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7facf-111">Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="7facf-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7facf-112">*пвсторепровфиндинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7facf-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7facf-113">Указатель на буфер, содержащий сведения о поиске.</span><span class="sxs-lookup"><span data-stu-id="7facf-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="7facf-114">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7facf-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7facf-115">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="7facf-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7facf-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7facf-116">Return value</span></span>

<span data-ttu-id="7facf-117">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="7facf-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7facf-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7facf-118">Requirements</span></span>



| <span data-ttu-id="7facf-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7facf-119">Requirement</span></span> | <span data-ttu-id="7facf-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7facf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7facf-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7facf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7facf-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7facf-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7facf-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7facf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7facf-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7facf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7facf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7facf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7facf-126">**цертсторепровфиндктл**</span><span class="sxs-lookup"><span data-stu-id="7facf-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="7facf-127">**\_контекст CTL**</span><span class="sxs-lookup"><span data-stu-id="7facf-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
