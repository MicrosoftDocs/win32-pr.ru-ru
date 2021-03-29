---
description: Выполняет сброс до начала последовательности перечисления.
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
ms.openlocfilehash: 60aeb1f68bcbf18e903472fa736b5714076dfbfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647956"
---
# <a name="ienumpstoretypesreset-method"></a><span data-ttu-id="f4010-103">Метод Иенумпсторетипес:: Reset</span><span class="sxs-lookup"><span data-stu-id="f4010-103">IEnumPStoreTypes::Reset method</span></span>

<span data-ttu-id="f4010-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f4010-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f4010-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="f4010-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f4010-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="f4010-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f4010-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f4010-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f4010-108">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="f4010-108">Resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4010-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4010-109">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="f4010-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4010-110">Parameters</span></span>

<span data-ttu-id="f4010-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f4010-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4010-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4010-112">Return value</span></span>

<span data-ttu-id="f4010-113">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4010-113">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4010-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f4010-114">Requirements</span></span>



| <span data-ttu-id="f4010-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f4010-115">Requirement</span></span> | <span data-ttu-id="f4010-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f4010-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4010-117">Header</span><span class="sxs-lookup"><span data-stu-id="f4010-117">Header</span></span><br/> | <dl> <span data-ttu-id="f4010-118"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4010-118"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f4010-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f4010-119">DLL</span></span><br/>    | <dl> <span data-ttu-id="f4010-120"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4010-120"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4010-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4010-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4010-122">**иенумпсторетипес**</span><span class="sxs-lookup"><span data-stu-id="f4010-122">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
