---
description: Возвращает значение масштаба стиппле-pattern.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'Метод ID3DXLine:: Жетпаттернскале (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424530"
---
# <a name="id3dxlinegetpatternscale-method"></a><span data-ttu-id="13fa9-103">Метод ID3DXLine:: Жетпаттернскале</span><span class="sxs-lookup"><span data-stu-id="13fa9-103">ID3DXLine::GetPatternScale method</span></span>

<span data-ttu-id="13fa9-104">Возвращает значение масштаба стиппле-pattern.</span><span class="sxs-lookup"><span data-stu-id="13fa9-104">Gets the stipple-pattern scale value.</span></span>

## <a name="syntax"></a><span data-ttu-id="13fa9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13fa9-105">Syntax</span></span>


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a><span data-ttu-id="13fa9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13fa9-106">Parameters</span></span>

<span data-ttu-id="13fa9-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="13fa9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13fa9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13fa9-108">Return value</span></span>

<span data-ttu-id="13fa9-109">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13fa9-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13fa9-110">Возвращает значение, используемое для масштабирования шаблона стиппле.</span><span class="sxs-lookup"><span data-stu-id="13fa9-110">Returns the value used to scale the stipple-pattern.</span></span> <span data-ttu-id="13fa9-111">1.0 f является значением по умолчанию и не представляет масштабирование.</span><span class="sxs-lookup"><span data-stu-id="13fa9-111">1.0f is the default value and represents no scaling.</span></span> <span data-ttu-id="13fa9-112">Значение меньше 1,0 f сжимает шаблон, а значение, превышающее 1,0, растягивает шаблон.</span><span class="sxs-lookup"><span data-stu-id="13fa9-112">A value less than 1.0f shrinks the pattern, and a value greater than 1.0 stretches the pattern.</span></span>

## <a name="requirements"></a><span data-ttu-id="13fa9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="13fa9-113">Requirements</span></span>



| <span data-ttu-id="13fa9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="13fa9-114">Requirement</span></span> | <span data-ttu-id="13fa9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="13fa9-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13fa9-116">Header</span><span class="sxs-lookup"><span data-stu-id="13fa9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="13fa9-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="13fa9-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="13fa9-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13fa9-118">Library</span></span><br/> | <dl> <span data-ttu-id="13fa9-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13fa9-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="13fa9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13fa9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13fa9-121">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="13fa9-121">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="13fa9-122">**ID3DXLine:: Сетпаттернскале**</span><span class="sxs-lookup"><span data-stu-id="13fa9-122">**ID3DXLine::SetPatternScale**</span></span>](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
