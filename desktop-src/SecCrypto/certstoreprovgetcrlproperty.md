---
description: Извлекает указанное свойство списка отзыва сертификатов.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Функция обратного вызова Цертсторепровжеткрлпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683292"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="b819f-103">Функция обратного вызова Цертсторепровжеткрлпроперти</span><span class="sxs-lookup"><span data-stu-id="b819f-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="b819f-104">Функция обратного вызова **цертсторепровжеткрлпроперти** извлекает указанное свойство [*списка отзыва сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b819f-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b819f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b819f-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="b819f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b819f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b819f-107">*хсторепров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b819f-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b819f-108">**Хцертсторепров** -обработчик в [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b819f-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="b819f-109">*пкрлконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b819f-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b819f-110">Указатель на структуру [**\_ контекста списка отзыва сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .</span><span class="sxs-lookup"><span data-stu-id="b819f-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b819f-111">*dwPropId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b819f-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b819f-112">Указывает идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="b819f-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b819f-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b819f-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b819f-114">Все необходимые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="b819f-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="b819f-115">*пвдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b819f-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b819f-116">Указатель на буфер, содержащий указатель на структуру [**\_ контекста списка отзыва сертификатов**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) , возвращаемую функцией.</span><span class="sxs-lookup"><span data-stu-id="b819f-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="b819f-117">При первом вызове функции может быть задано значение **null** , чтобы получить значение *пкбдата* перед выделением памяти для буфера.</span><span class="sxs-lookup"><span data-stu-id="b819f-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b819f-118">*пкбдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b819f-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b819f-119">Указатель на **DWORD** , указывающий длину буфера *пвдата* .</span><span class="sxs-lookup"><span data-stu-id="b819f-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b819f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b819f-120">Return value</span></span>

<span data-ttu-id="b819f-121">Возвращает **значение true** , если функция завершается успешно, или **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="b819f-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="b819f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="b819f-122">Requirements</span></span>



| <span data-ttu-id="b819f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="b819f-123">Requirement</span></span> | <span data-ttu-id="b819f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b819f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b819f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b819f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b819f-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b819f-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b819f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b819f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b819f-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b819f-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b819f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b819f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b819f-130">**Контекст списка отзыва сертификатов \_**</span><span class="sxs-lookup"><span data-stu-id="b819f-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
