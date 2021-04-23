---
description: Возвращает имя анимации по заданному индексу.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'Метод ID3DXAnimationSet:: Жетаниматионнамебиндекс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703865"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a><span data-ttu-id="4bc2a-103">Метод ID3DXAnimationSet:: Жетаниматионнамебиндекс</span><span class="sxs-lookup"><span data-stu-id="4bc2a-103">ID3DXAnimationSet::GetAnimationNameByIndex method</span></span>

<span data-ttu-id="4bc2a-104">Возвращает имя анимации по заданному индексу.</span><span class="sxs-lookup"><span data-stu-id="4bc2a-104">Gets the name of an animation, given its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc2a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bc2a-105">Syntax</span></span>


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="4bc2a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bc2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc2a-107">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4bc2a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc2a-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bc2a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bc2a-109">Индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="4bc2a-109">Index of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="4bc2a-110">*ппнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4bc2a-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc2a-111">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4bc2a-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4bc2a-112">Адрес указателя на строку, которая получает имя анимации.</span><span class="sxs-lookup"><span data-stu-id="4bc2a-112">Address of a pointer to a string that receives the animation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc2a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bc2a-113">Return value</span></span>

<span data-ttu-id="4bc2a-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4bc2a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4bc2a-115">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="4bc2a-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="4bc2a-116">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="4bc2a-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="4bc2a-117">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="4bc2a-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc2a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4bc2a-118">Requirements</span></span>



| <span data-ttu-id="4bc2a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4bc2a-119">Requirement</span></span> | <span data-ttu-id="4bc2a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4bc2a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc2a-121">Header</span><span class="sxs-lookup"><span data-stu-id="4bc2a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4bc2a-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bc2a-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4bc2a-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4bc2a-123">Library</span></span><br/> | <dl> <span data-ttu-id="4bc2a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bc2a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bc2a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bc2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc2a-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4bc2a-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
