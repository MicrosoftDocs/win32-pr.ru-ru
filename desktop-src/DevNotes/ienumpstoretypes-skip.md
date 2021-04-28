---
description: 'Метод Иенумпсторетипес:: Skip — пропускает следующее заданное число элементов в последовательности перечисления.'
ms.assetid: 4c02aac8-0496-4ad9-9863-2074b2c71902
title: 'Метод Иенумпсторетипес:: Skip (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: fdc656af2a8f50d02d2f88545d189d9c9285a7f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096742"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="b08a2-103">Метод Иенумпсторетипес:: Skip</span><span class="sxs-lookup"><span data-stu-id="b08a2-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="b08a2-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b08a2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b08a2-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="b08a2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b08a2-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="b08a2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b08a2-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b08a2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b08a2-108">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="b08a2-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b08a2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b08a2-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="b08a2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b08a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b08a2-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b08a2-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b08a2-112">Число типов поставщиков для пропуска.</span><span class="sxs-lookup"><span data-stu-id="b08a2-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b08a2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b08a2-113">Return value</span></span>

<span data-ttu-id="b08a2-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b08a2-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b08a2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b08a2-115">Requirements</span></span>



| <span data-ttu-id="b08a2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b08a2-116">Requirement</span></span> | <span data-ttu-id="b08a2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b08a2-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b08a2-118">Header</span><span class="sxs-lookup"><span data-stu-id="b08a2-118">Header</span></span><br/> | <dl> <span data-ttu-id="b08a2-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b08a2-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b08a2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b08a2-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="b08a2-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b08a2-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b08a2-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b08a2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b08a2-123">**иенумпсторетипес**</span><span class="sxs-lookup"><span data-stu-id="b08a2-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
