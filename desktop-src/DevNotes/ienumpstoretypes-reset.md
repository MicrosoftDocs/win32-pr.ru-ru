---
description: 'Метод Иенумпсторетипес:: Reset — сбрасывается до начала последовательности перечисления.'
ms.assetid: 35f14aa5-92cb-4ad8-b80c-2550dedb7a7f
title: 'Метод Иенумпсторетипес:: Reset (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Reset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 55953a67d19ac94f792769974d860bae9b57f1ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089322"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="904b6-103">Метод Иенумпсторетипес:: Reset</span><span class="sxs-lookup"><span data-stu-id="904b6-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="904b6-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="904b6-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="904b6-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="904b6-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="904b6-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="904b6-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="904b6-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="904b6-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="904b6-108">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="904b6-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="904b6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="904b6-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="904b6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="904b6-110">Parameters</span></span>

<span data-ttu-id="904b6-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="904b6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="904b6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="904b6-112">Return value</span></span>

<span data-ttu-id="904b6-113">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="904b6-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="904b6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="904b6-114">Requirements</span></span>



| <span data-ttu-id="904b6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="904b6-115">Requirement</span></span> | <span data-ttu-id="904b6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="904b6-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="904b6-117">Header</span><span class="sxs-lookup"><span data-stu-id="904b6-117">Header</span></span><br/> | <dl> <span data-ttu-id="904b6-118"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="904b6-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="904b6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="904b6-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="904b6-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="904b6-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904b6-121">См. также</span><span class="sxs-lookup"><span data-stu-id="904b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904b6-122">**иенумпсторетипес**</span><span class="sxs-lookup"><span data-stu-id="904b6-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
