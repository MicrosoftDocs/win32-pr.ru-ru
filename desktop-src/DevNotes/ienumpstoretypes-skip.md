---
description: Пропускает следующее заданное число элементов в последовательности перечисления.
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
ms.openlocfilehash: 511595dd55f66e91ae0f5606f9e047918e7ff0fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649029"
---
# <a name="ienumpstoretypesskip-method"></a><span data-ttu-id="07719-103">Метод Иенумпсторетипес:: Skip</span><span class="sxs-lookup"><span data-stu-id="07719-103">IEnumPStoreTypes::Skip method</span></span>

<span data-ttu-id="07719-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="07719-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="07719-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="07719-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="07719-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="07719-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="07719-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="07719-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="07719-108">Пропускает следующее заданное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="07719-108">Skips over the next specified number of items in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="07719-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07719-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a><span data-ttu-id="07719-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="07719-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07719-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07719-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07719-112">Число типов поставщиков для пропуска.</span><span class="sxs-lookup"><span data-stu-id="07719-112">The number of provider types to be skipped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07719-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07719-113">Return value</span></span>

<span data-ttu-id="07719-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07719-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="07719-115">Требования</span><span class="sxs-lookup"><span data-stu-id="07719-115">Requirements</span></span>



| <span data-ttu-id="07719-116">Требование</span><span class="sxs-lookup"><span data-stu-id="07719-116">Requirement</span></span> | <span data-ttu-id="07719-117">Значение</span><span class="sxs-lookup"><span data-stu-id="07719-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07719-118">Header</span><span class="sxs-lookup"><span data-stu-id="07719-118">Header</span></span><br/> | <dl> <span data-ttu-id="07719-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="07719-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="07719-120">DLL</span><span class="sxs-lookup"><span data-stu-id="07719-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="07719-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07719-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07719-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07719-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07719-123">**иенумпсторетипес**</span><span class="sxs-lookup"><span data-stu-id="07719-123">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
