---
description: Возвращает указанное число следующих имен элементов данных в последовательности перечисления.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: 'Метод Иенумпстореитемс:: Next (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 967f2f84553b87965d5b2c92d99e347cb259264b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649013"
---
# <a name="ienumpstoreitemsnext-method"></a><span data-ttu-id="761c6-103">Метод Иенумпстореитемс:: Next</span><span class="sxs-lookup"><span data-stu-id="761c6-103">IEnumPStoreItems::Next method</span></span>

<span data-ttu-id="761c6-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="761c6-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="761c6-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="761c6-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="761c6-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="761c6-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="761c6-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="761c6-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="761c6-108">Возвращает указанное число следующих имен элементов данных в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="761c6-108">Gets the next specified number of data item names in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="761c6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="761c6-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="761c6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="761c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="761c6-111">*celt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="761c6-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="761c6-112">Количество запрошенных элементов данных.</span><span class="sxs-lookup"><span data-stu-id="761c6-112">The number of data items requested.</span></span>

</dd> <dt>

<span data-ttu-id="761c6-113">*rgelt* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="761c6-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="761c6-114">Указатель на строку, в которой возвращается имя элемента данных.</span><span class="sxs-lookup"><span data-stu-id="761c6-114">A pointer to a string in which to return the data item name.</span></span>

</dd> <dt>

<span data-ttu-id="761c6-115">*пцелтфетчед* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="761c6-115">*pceltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="761c6-116">Указатель на число фактически предоставляемых имен элементов данных.</span><span class="sxs-lookup"><span data-stu-id="761c6-116">A pointer to the number of data item names actually supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="761c6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="761c6-117">Return value</span></span>

<span data-ttu-id="761c6-118">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="761c6-118">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="761c6-119">Требования</span><span class="sxs-lookup"><span data-stu-id="761c6-119">Requirements</span></span>



| <span data-ttu-id="761c6-120">Требование</span><span class="sxs-lookup"><span data-stu-id="761c6-120">Requirement</span></span> | <span data-ttu-id="761c6-121">Значение</span><span class="sxs-lookup"><span data-stu-id="761c6-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="761c6-122">Header</span><span class="sxs-lookup"><span data-stu-id="761c6-122">Header</span></span><br/> | <dl> <span data-ttu-id="761c6-123"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="761c6-123"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="761c6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="761c6-124">DLL</span></span><br/>    | <dl> <span data-ttu-id="761c6-125"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="761c6-125"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="761c6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="761c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761c6-127">**иенумпстореитемс**</span><span class="sxs-lookup"><span data-stu-id="761c6-127">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
