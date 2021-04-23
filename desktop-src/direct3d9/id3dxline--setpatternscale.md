---
description: Растягивает шаблон стиппле вдоль направления линии.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'Метод ID3DXLine:: Сетпаттернскале (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44c040a2e8899784bcea9b93bf0781afb39c2464
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273975"
---
# <a name="id3dxlinesetpatternscale-method"></a><span data-ttu-id="c1d9e-103">Метод ID3DXLine:: Сетпаттернскале</span><span class="sxs-lookup"><span data-stu-id="c1d9e-103">ID3DXLine::SetPatternScale method</span></span>

<span data-ttu-id="c1d9e-104">Растягивает шаблон стиппле вдоль направления линии.</span><span class="sxs-lookup"><span data-stu-id="c1d9e-104">Stretches the stipple pattern along the line direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d9e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1d9e-105">Syntax</span></span>


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a><span data-ttu-id="c1d9e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1d9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d9e-107">*фпаттернскале* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1d9e-107">*fPatternScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1d9e-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c1d9e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c1d9e-109">Значение масштабирования шаблона стиппле.</span><span class="sxs-lookup"><span data-stu-id="c1d9e-109">Stipple pattern scaling value.</span></span> <span data-ttu-id="c1d9e-110">1.0 f является значением по умолчанию и не представляет масштабирование.</span><span class="sxs-lookup"><span data-stu-id="c1d9e-110">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="c1d9e-111">Значение меньше 1,0 f сжимает шаблон, а значение, превышающее 1,0, растягивает шаблон.</span><span class="sxs-lookup"><span data-stu-id="c1d9e-111">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1d9e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1d9e-112">Return value</span></span>

<span data-ttu-id="c1d9e-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c1d9e-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c1d9e-114">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c1d9e-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c1d9e-115">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="c1d9e-115">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d9e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c1d9e-116">Requirements</span></span>



| <span data-ttu-id="c1d9e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c1d9e-117">Requirement</span></span> | <span data-ttu-id="c1d9e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c1d9e-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d9e-119">Header</span><span class="sxs-lookup"><span data-stu-id="c1d9e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c1d9e-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d9e-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c1d9e-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c1d9e-121">Library</span></span><br/> | <dl> <span data-ttu-id="c1d9e-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1d9e-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1d9e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1d9e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d9e-124">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="c1d9e-124">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
