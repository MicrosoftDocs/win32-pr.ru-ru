---
description: 'Метод Иенумпсторепровидерс:: Skip — пропускает следующее заданное число элементов в последовательности перечисления.'
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'Метод Иенумпсторепровидерс:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096752"
---
# <a name="ienumpstoreprovidersskip-method"></a><span data-ttu-id="d43f6-103">Метод Иенумпсторепровидерс:: Skip</span><span class="sxs-lookup"><span data-stu-id="d43f6-103">IEnumPStoreProviders::Skip method</span></span>

<span data-ttu-id="d43f6-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d43f6-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d43f6-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="d43f6-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d43f6-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="d43f6-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d43f6-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d43f6-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d43f6-108">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="d43f6-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43f6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d43f6-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="d43f6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d43f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d43f6-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d43f6-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d43f6-112">Число типов поставщиков для пропуска.</span><span class="sxs-lookup"><span data-stu-id="d43f6-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d43f6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d43f6-113">Return value</span></span>

<span data-ttu-id="d43f6-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d43f6-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43f6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="d43f6-115">Requirements</span></span>



| <span data-ttu-id="d43f6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="d43f6-116">Requirement</span></span> | <span data-ttu-id="d43f6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d43f6-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d43f6-118">Header</span><span class="sxs-lookup"><span data-stu-id="d43f6-118">Header</span></span><br/> | <dl> <span data-ttu-id="d43f6-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d43f6-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d43f6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d43f6-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="d43f6-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d43f6-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d43f6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d43f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43f6-123">**иенумпсторепровидерс**</span><span class="sxs-lookup"><span data-stu-id="d43f6-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
