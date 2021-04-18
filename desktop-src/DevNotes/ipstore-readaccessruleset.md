---
description: Считывает правила доступа для заданного типа.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'Метод Ипсторе:: Реадакцессрулесет (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648876"
---
# <a name="ipstorereadaccessruleset-method"></a><span data-ttu-id="e9e8c-103">Метод Ипсторе:: Реадакцессрулесет</span><span class="sxs-lookup"><span data-stu-id="e9e8c-103">IPStore::ReadAccessRuleSet method</span></span>

<span data-ttu-id="e9e8c-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e9e8c-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e9e8c-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e9e8c-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e9e8c-108">\[Этот метод не реализован.\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="e9e8c-109">Считывает правила доступа для заданного типа.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-109">Reads the access rules for a given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e8c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9e8c-110">Syntax</span></span>


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e9e8c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9e8c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e8c-112">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e8c-113">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8c-114">*птипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e8c-115">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8c-116">*псубтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e8c-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8c-118">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e8c-119">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8c-120">*ппрулес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-120">*ppRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e8c-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e9e8c-122">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9e8c-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e8c-123">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e8c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9e8c-124">Return value</span></span>

<span data-ttu-id="e9e8c-125">Вызовы этого метода всегда завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e9e8c-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e8c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e9e8c-126">Requirements</span></span>



| <span data-ttu-id="e9e8c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e9e8c-127">Requirement</span></span> | <span data-ttu-id="e9e8c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e9e8c-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e8c-129">Header</span><span class="sxs-lookup"><span data-stu-id="e9e8c-129">Header</span></span><br/> | <dl> <span data-ttu-id="e9e8c-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9e8c-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="e9e8c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e9e8c-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="e9e8c-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9e8c-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e8c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9e8c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e8c-134">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="e9e8c-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
