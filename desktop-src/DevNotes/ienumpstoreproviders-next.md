---
description: Возвращает указанное число следующих поставщиков в последовательности перечисления.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'Метод Иенумпсторепровидерс:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f468d29682c4e3767d4d8fe7d59e60976f103484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648084"
---
# <a name="ienumpstoreprovidersnext-method"></a><span data-ttu-id="ffd85-103">Метод Иенумпсторепровидерс:: Next</span><span class="sxs-lookup"><span data-stu-id="ffd85-103">IEnumPStoreProviders::Next method</span></span>

<span data-ttu-id="ffd85-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffd85-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ffd85-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="ffd85-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ffd85-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="ffd85-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ffd85-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ffd85-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ffd85-108">Возвращает указанное число следующих поставщиков в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="ffd85-108">Gets the next specified number of providers in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd85-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffd85-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ffd85-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffd85-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd85-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ffd85-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd85-112">Число запрошенных типов поставщиков.</span><span class="sxs-lookup"><span data-stu-id="ffd85-112">The number of provider types requested.</span></span>

</dd> <dt>

<span data-ttu-id="ffd85-113">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ffd85-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd85-114">Указатель на строку, в которой возвращается имя типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="ffd85-114">A pointer to a string in which to return the provider type name.</span></span>

</dd> <dt>

<span data-ttu-id="ffd85-115">*пцелтфетчед* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="ffd85-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffd85-116">Указатель на число типов поставщиков, которые были переданы фактически.</span><span class="sxs-lookup"><span data-stu-id="ffd85-116">A pointer to the number of provider types that was actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd85-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffd85-117">Return value</span></span>

<span data-ttu-id="ffd85-118">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ffd85-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd85-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ffd85-119">Requirements</span></span>



| <span data-ttu-id="ffd85-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ffd85-120">Requirement</span></span> | <span data-ttu-id="ffd85-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ffd85-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd85-122">Header</span><span class="sxs-lookup"><span data-stu-id="ffd85-122">Header</span></span><br/> | <dl> <span data-ttu-id="ffd85-123"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd85-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ffd85-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ffd85-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="ffd85-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffd85-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffd85-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffd85-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd85-127">**иенумпсторепровидерс**</span><span class="sxs-lookup"><span data-stu-id="ffd85-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
