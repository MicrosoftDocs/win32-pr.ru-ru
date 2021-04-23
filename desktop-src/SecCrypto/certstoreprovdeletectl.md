---
description: Вызывается методом Цертделетектлфромсторе перед удалением списка доверия сертификатов из хранилища.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Функция обратного вызова Цертсторепровделетектл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908971"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="603d7-103">Функция обратного вызова Цертсторепровделетектл</span><span class="sxs-lookup"><span data-stu-id="603d7-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="603d7-104">Функция обратного вызова **цертсторепровделетектл** вызывается [**цертделетектлфромсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) перед удалением списка доверия сертификатов из хранилища.</span><span class="sxs-lookup"><span data-stu-id="603d7-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="603d7-105">Эта функция определяет, можно ли удалить список доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="603d7-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="603d7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="603d7-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="603d7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="603d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603d7-108">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="603d7-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="603d7-109">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="603d7-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="603d7-110">*пктлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="603d7-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="603d7-111">Указатель на структуру [**\_ контекста CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="603d7-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="603d7-112">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="603d7-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="603d7-113">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="603d7-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603d7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="603d7-114">Return value</span></span>

<span data-ttu-id="603d7-115">Возвращает **значение true** , если список доверия сертификатов можно удалить из хранилища.</span><span class="sxs-lookup"><span data-stu-id="603d7-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="603d7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="603d7-116">Requirements</span></span>



| <span data-ttu-id="603d7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="603d7-117">Requirement</span></span> | <span data-ttu-id="603d7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="603d7-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="603d7-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="603d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="603d7-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="603d7-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="603d7-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="603d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="603d7-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="603d7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
