---
description: Создает другой перечислитель с тем же состоянием перечисления, что и текущий.
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'Метод Иенумпсторепровидерс:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdd7825a44dcea672eff24a15126921f0426a986
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648804"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="d6cf3-103">Метод Иенумпсторепровидерс:: Clone</span><span class="sxs-lookup"><span data-stu-id="d6cf3-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="d6cf3-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6cf3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d6cf3-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="d6cf3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d6cf3-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="d6cf3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d6cf3-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d6cf3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d6cf3-108">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="d6cf3-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6cf3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6cf3-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="d6cf3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6cf3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6cf3-111">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d6cf3-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6cf3-112">Указатель на указатель [**иенумпсторепровидерс**](ienumpstoreproviders.md) .</span><span class="sxs-lookup"><span data-stu-id="d6cf3-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6cf3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6cf3-113">Return value</span></span>

<span data-ttu-id="d6cf3-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6cf3-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6cf3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d6cf3-115">Requirements</span></span>



| <span data-ttu-id="d6cf3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d6cf3-116">Requirement</span></span> | <span data-ttu-id="d6cf3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d6cf3-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6cf3-118">Header</span><span class="sxs-lookup"><span data-stu-id="d6cf3-118">Header</span></span><br/> | <dl> <span data-ttu-id="d6cf3-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6cf3-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d6cf3-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d6cf3-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="d6cf3-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6cf3-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6cf3-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6cf3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6cf3-123">**иенумпсторепровидерс**</span><span class="sxs-lookup"><span data-stu-id="d6cf3-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
