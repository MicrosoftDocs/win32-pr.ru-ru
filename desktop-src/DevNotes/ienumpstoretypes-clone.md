---
description: Создает дополнительный перечислитель, который содержит то же состояние перечисления, что и текущий.
ms.assetid: b4027520-62cc-40d4-b9fd-01fa9c652a54
title: 'Метод Иенумпсторетипес:: Clone (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4ac088ae708b62f458d7bba52127dadc8ef77c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657900"
---
# <a name="ienumpstoretypesclone-method"></a><span data-ttu-id="e4668-103">Метод Иенумпсторетипес:: Clone</span><span class="sxs-lookup"><span data-stu-id="e4668-103">IEnumPStoreTypes::Clone method</span></span>

<span data-ttu-id="e4668-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e4668-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e4668-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="e4668-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e4668-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="e4668-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e4668-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="e4668-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e4668-108">Создает дополнительный перечислитель, который содержит то же состояние перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="e4668-108">Creates an additional enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4668-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4668-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="e4668-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4668-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4668-111">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4668-111">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4668-112">Указатель на указатель [**иенумпстореитемс**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="e4668-112">A pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4668-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4668-113">Return value</span></span>

<span data-ttu-id="e4668-114">Возвращаемое значение является значением **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4668-114">The return value is an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4668-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e4668-115">Requirements</span></span>



| <span data-ttu-id="e4668-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e4668-116">Requirement</span></span> | <span data-ttu-id="e4668-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e4668-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4668-118">Header</span><span class="sxs-lookup"><span data-stu-id="e4668-118">Header</span></span><br/> | <dl> <span data-ttu-id="e4668-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4668-119"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="e4668-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e4668-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="e4668-121"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4668-121"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4668-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4668-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4668-123">**иенумпстореитемс**</span><span class="sxs-lookup"><span data-stu-id="e4668-123">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
</dt> <dt>

[<span data-ttu-id="e4668-124">**иенумпсторетипес**</span><span class="sxs-lookup"><span data-stu-id="e4668-124">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
</dt> </dl>

 

 
