---
description: Предназначен для установки указанных сведений о параметрах.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'Метод Ипсторе:: Жетпровпарам (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ac45c08f64658d176449d76456e737a1a37dc2b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647955"
---
# <a name="ipstoregetprovparam-method"></a><span data-ttu-id="de727-103">Метод Ипсторе:: Жетпровпарам</span><span class="sxs-lookup"><span data-stu-id="de727-103">IPStore::GetProvParam method</span></span>

<span data-ttu-id="de727-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="de727-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="de727-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="de727-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="de727-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="de727-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="de727-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="de727-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="de727-108">\[Этот метод не реализован.\]</span><span class="sxs-lookup"><span data-stu-id="de727-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="de727-109">Предназначен для установки указанных сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="de727-109">Intended to set the specified parameter information.</span></span> <span data-ttu-id="de727-110">Однако обратите внимание, что она не реализована и всегда завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="de727-110">Note, however, that it is not implemented and will always fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="de727-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de727-111">Syntax</span></span>


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="de727-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="de727-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de727-113">*двпарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de727-113">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de727-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="de727-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="de727-115">*пкбдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de727-115">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de727-116">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="de727-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="de727-117">*ппбдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de727-117">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de727-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="de727-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="de727-119">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de727-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de727-120">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="de727-120">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de727-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de727-121">Return value</span></span>

<span data-ttu-id="de727-122">Вызовы этого метода всегда завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="de727-122">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="de727-123">Требования</span><span class="sxs-lookup"><span data-stu-id="de727-123">Requirements</span></span>



| <span data-ttu-id="de727-124">Требование</span><span class="sxs-lookup"><span data-stu-id="de727-124">Requirement</span></span> | <span data-ttu-id="de727-125">Значение</span><span class="sxs-lookup"><span data-stu-id="de727-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de727-126">Header</span><span class="sxs-lookup"><span data-stu-id="de727-126">Header</span></span><br/> | <dl> <span data-ttu-id="de727-127"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="de727-127"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="de727-128">DLL</span><span class="sxs-lookup"><span data-stu-id="de727-128">DLL</span></span><br/>    | <dl> <span data-ttu-id="de727-129"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de727-129"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de727-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de727-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de727-131">**ипсторе**</span><span class="sxs-lookup"><span data-stu-id="de727-131">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
