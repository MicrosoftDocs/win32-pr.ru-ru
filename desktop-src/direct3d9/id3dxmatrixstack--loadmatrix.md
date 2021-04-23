---
description: Загружает заданную матрицу в текущую матрицу.
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'Метод ID3DXMATRIXStack:: Лоадматрикс (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 292b4e147dfa99023f0b4d560a4ed41e6b41b3fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547839"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="36069-103">Метод ID3DXMATRIXStack:: Лоадматрикс (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="36069-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="36069-104">Загружает заданную матрицу в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="36069-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="36069-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36069-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="36069-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36069-107">*пмат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36069-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36069-108">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="36069-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="36069-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , загруженную в текущую матрицу.</span><span class="sxs-lookup"><span data-stu-id="36069-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36069-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36069-110">Return value</span></span>

<span data-ttu-id="36069-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36069-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36069-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="36069-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="36069-113">В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="36069-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="36069-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36069-114">Remarks</span></span>

<span data-ttu-id="36069-115">Обратите внимание, что этот метод не добавляет элемент в стек; Вместо этого он заменяет текущую матрицу представленной матрицей.</span><span class="sxs-lookup"><span data-stu-id="36069-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="36069-116">Требования</span><span class="sxs-lookup"><span data-stu-id="36069-116">Requirements</span></span>



| <span data-ttu-id="36069-117">Требование</span><span class="sxs-lookup"><span data-stu-id="36069-117">Requirement</span></span> | <span data-ttu-id="36069-118">Значение</span><span class="sxs-lookup"><span data-stu-id="36069-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36069-119">Header</span><span class="sxs-lookup"><span data-stu-id="36069-119">Header</span></span><br/>  | <dl> <span data-ttu-id="36069-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="36069-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="36069-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36069-121">Library</span></span><br/> | <dl> <span data-ttu-id="36069-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36069-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36069-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36069-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36069-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="36069-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="36069-125">**ID3DXMATRIXStack:: Лоадидентити**</span><span class="sxs-lookup"><span data-stu-id="36069-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




