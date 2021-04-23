---
description: 'Завершает срок существования указателя Ппдата, возвращенного ID3DXFileData:: Lock.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'Метод ID3DXFileData:: Unlock (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821212"
---
# <a name="id3dxfiledataunlock-method"></a><span data-ttu-id="d2299-103">Метод ID3DXFileData:: Unlock</span><span class="sxs-lookup"><span data-stu-id="d2299-103">ID3DXFileData::Unlock method</span></span>

<span data-ttu-id="d2299-104">Завершает срок существования указателя *ппдата* , возвращенного [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="d2299-104">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2299-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2299-105">Syntax</span></span>


```C++
BOOL Unlock();
```



## <a name="parameters"></a><span data-ttu-id="d2299-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2299-106">Parameters</span></span>

<span data-ttu-id="d2299-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d2299-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2299-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2299-108">Return value</span></span>

<span data-ttu-id="d2299-109">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2299-109">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2299-110">Возвращаемое значение — S \_ .</span><span class="sxs-lookup"><span data-stu-id="d2299-110">The return value is S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2299-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2299-111">Remarks</span></span>

<span data-ttu-id="d2299-112">Необходимо убедиться, что число вызовов [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) соответствует числу вызовов **ID3DXFileData:: Unlock** .</span><span class="sxs-lookup"><span data-stu-id="d2299-112">You must ensure that the number of [**ID3DXFileData::Lock**](id3dxfiledata--lock.md) calls matches the number of **ID3DXFileData::Unlock** calls.</span></span> <span data-ttu-id="d2299-113">После вызова функции Unlock указатель Ппдата, возвращенный **ID3DXFileData:: Lock** , больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="d2299-113">After calling Unlock, the ppData pointer returned by **ID3DXFileData::Lock** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2299-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d2299-114">Requirements</span></span>



| <span data-ttu-id="d2299-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d2299-115">Requirement</span></span> | <span data-ttu-id="d2299-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d2299-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2299-117">Header</span><span class="sxs-lookup"><span data-stu-id="d2299-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d2299-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2299-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d2299-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d2299-119">Library</span></span><br/> | <dl> <span data-ttu-id="d2299-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2299-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d2299-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2299-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2299-122">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="d2299-122">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
