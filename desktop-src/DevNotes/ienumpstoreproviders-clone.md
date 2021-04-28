---
description: 'Метод Иенумпсторепровидерс:: Clone — создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.'
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
ms.openlocfilehash: 2eb5f5788c903c854d9cf1551d6cf5a1bd2b51f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096802"
---
# <a name="ienumpstoreprovidersclone-method"></a><span data-ttu-id="24e22-103">Метод Иенумпсторепровидерс:: Clone</span><span class="sxs-lookup"><span data-stu-id="24e22-103">IEnumPStoreProviders::Clone method</span></span>

<span data-ttu-id="24e22-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24e22-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="24e22-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="24e22-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="24e22-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="24e22-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="24e22-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="24e22-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="24e22-108">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="24e22-108">Creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="24e22-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24e22-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="24e22-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="24e22-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e22-111">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="24e22-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24e22-112">Указатель на указатель [**иенумпсторепровидерс**](ienumpstoreproviders.md) .</span><span class="sxs-lookup"><span data-stu-id="24e22-112">A pointer to an [**IEnumPStoreProviders**](ienumpstoreproviders.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e22-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24e22-113">Return value</span></span>

<span data-ttu-id="24e22-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24e22-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e22-115">Требования</span><span class="sxs-lookup"><span data-stu-id="24e22-115">Requirements</span></span>



| <span data-ttu-id="24e22-116">Требование</span><span class="sxs-lookup"><span data-stu-id="24e22-116">Requirement</span></span> | <span data-ttu-id="24e22-117">Значение</span><span class="sxs-lookup"><span data-stu-id="24e22-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e22-118">Header</span><span class="sxs-lookup"><span data-stu-id="24e22-118">Header</span></span><br/> | <dl> <span data-ttu-id="24e22-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="24e22-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="24e22-120">DLL</span><span class="sxs-lookup"><span data-stu-id="24e22-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="24e22-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e22-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e22-122">См. также</span><span class="sxs-lookup"><span data-stu-id="24e22-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e22-123">**иенумпсторепровидерс**</span><span class="sxs-lookup"><span data-stu-id="24e22-123">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
</dt> </dl>

 

 
