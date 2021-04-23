---
description: Создает другой перечислитель с тем же состоянием перечисления, что и текущий.
ms.assetid: ab9eaf63-54e4-4322-9bb5-227982b15c73
title: 'Метод Иенумпстореитемс:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 919c0359f5c7f6d3ab547f53a105246c43e20fb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657878"
---
# <a name="ienumpstoreitemsclone-method"></a><span data-ttu-id="6c5f9-103">Метод Иенумпстореитемс:: Clone</span><span class="sxs-lookup"><span data-stu-id="6c5f9-103">IEnumPStoreItems::Clone method</span></span>

<span data-ttu-id="6c5f9-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6c5f9-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6c5f9-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6c5f9-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="6c5f9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6c5f9-108">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="6c5f9-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5f9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c5f9-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="6c5f9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c5f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5f9-111">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6c5f9-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5f9-112">Указатель на указатель [**иенумпстореитемс**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="6c5f9-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5f9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c5f9-113">Return value</span></span>

<span data-ttu-id="6c5f9-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c5f9-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5f9-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6c5f9-115">Requirements</span></span>



| <span data-ttu-id="6c5f9-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6c5f9-116">Requirement</span></span> | <span data-ttu-id="6c5f9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6c5f9-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5f9-118">Header</span><span class="sxs-lookup"><span data-stu-id="6c5f9-118">Header</span></span><br/> | <dl> <span data-ttu-id="6c5f9-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5f9-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6c5f9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6c5f9-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="6c5f9-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5f9-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5f9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c5f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5f9-123">**иенумпстореитемс**</span><span class="sxs-lookup"><span data-stu-id="6c5f9-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> </dl>

 

 
