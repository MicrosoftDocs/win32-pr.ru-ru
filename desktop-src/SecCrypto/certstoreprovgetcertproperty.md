---
description: Извлекает указанное свойство сертификата.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Функция обратного вызова Цертсторепровжетцертпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662891"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="e8c25-103">Функция обратного вызова Цертсторепровжетцертпроперти</span><span class="sxs-lookup"><span data-stu-id="e8c25-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="e8c25-104">Функция обратного вызова **цертсторепровжетцертпроперти** извлекает указанное свойство сертификата.</span><span class="sxs-lookup"><span data-stu-id="e8c25-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c25-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8c25-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="e8c25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8c25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c25-107">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c25-108">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e8c25-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8c25-109">*пцертконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c25-110">Указатель на структуру [**\_ контекста сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="e8c25-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e8c25-111">*dwPropId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c25-112">Указывает идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="e8c25-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8c25-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c25-114">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="e8c25-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="e8c25-115">*пвдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c25-116">Указатель на буфер, содержащий указатель на структуру [**\_ контекста сертификата**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) , возвращаемую функцией.</span><span class="sxs-lookup"><span data-stu-id="e8c25-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="e8c25-117">При первом вызове функции может быть задано значение **null** , чтобы получить значение *пкбдата* перед выделением памяти для буфера.</span><span class="sxs-lookup"><span data-stu-id="e8c25-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e8c25-118">*пкбдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c25-119">Указатель на **DWORD** , указывающий длину буфера *пвдата* .</span><span class="sxs-lookup"><span data-stu-id="e8c25-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c25-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8c25-120">Return value</span></span>

<span data-ttu-id="e8c25-121">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="e8c25-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c25-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e8c25-122">Requirements</span></span>



| <span data-ttu-id="e8c25-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e8c25-123">Requirement</span></span> | <span data-ttu-id="e8c25-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e8c25-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e8c25-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8c25-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c25-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e8c25-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8c25-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c25-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8c25-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8c25-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8c25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c25-130">**\_контекст сертификата**</span><span class="sxs-lookup"><span data-stu-id="e8c25-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
