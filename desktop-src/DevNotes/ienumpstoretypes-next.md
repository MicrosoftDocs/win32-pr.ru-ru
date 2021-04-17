---
description: Возвращает указанное число следующих типов поставщиков в последовательности перечисления.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'Метод Иенумпсторетипес:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 18981053de897b75d1febdc75e138e6561e65bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657899"
---
# <a name="ienumpstoretypesnext-method"></a><span data-ttu-id="dbf92-103">Метод Иенумпсторетипес:: Next</span><span class="sxs-lookup"><span data-stu-id="dbf92-103">IEnumPStoreTypes::Next method</span></span>

<span data-ttu-id="dbf92-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dbf92-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="dbf92-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="dbf92-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="dbf92-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="dbf92-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="dbf92-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="dbf92-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="dbf92-108">Возвращает указанное число следующих типов поставщиков в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="dbf92-108">Gets the next specified number of provider types in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf92-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbf92-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="dbf92-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dbf92-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf92-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dbf92-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf92-112">Число запрошенных типов поставщиков.</span><span class="sxs-lookup"><span data-stu-id="dbf92-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="dbf92-113">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dbf92-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf92-114">Указатель на строку, в которой возвращается имя типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="dbf92-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="dbf92-115">*пцелтфетчед* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dbf92-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf92-116">Указатель на число фактически предоставляемых типов поставщиков.</span><span class="sxs-lookup"><span data-stu-id="dbf92-116">A pointer to the number of provider types actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf92-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dbf92-117">Return value</span></span>

<span data-ttu-id="dbf92-118">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbf92-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf92-119">Требования</span><span class="sxs-lookup"><span data-stu-id="dbf92-119">Requirements</span></span>



| <span data-ttu-id="dbf92-120">Требование</span><span class="sxs-lookup"><span data-stu-id="dbf92-120">Requirement</span></span> | <span data-ttu-id="dbf92-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dbf92-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf92-122">Header</span><span class="sxs-lookup"><span data-stu-id="dbf92-122">Header</span></span><br/> | <dl> <span data-ttu-id="dbf92-123"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf92-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="dbf92-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dbf92-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="dbf92-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbf92-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbf92-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbf92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf92-127">**иенумпсторетипес**</span><span class="sxs-lookup"><span data-stu-id="dbf92-127">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
