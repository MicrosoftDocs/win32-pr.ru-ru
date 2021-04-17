---
description: Возвращает индекс анимации по ее имени.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'Метод ID3DXAnimationSet:: Жетаниматиониндексбинаме (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703687"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="379c8-103">Метод ID3DXAnimationSet:: Жетаниматиониндексбинаме</span><span class="sxs-lookup"><span data-stu-id="379c8-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="379c8-104">Возвращает индекс анимации по ее имени.</span><span class="sxs-lookup"><span data-stu-id="379c8-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="379c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="379c8-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="379c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="379c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="379c8-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="379c8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="379c8-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="379c8-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="379c8-109">Имя анимации.</span><span class="sxs-lookup"><span data-stu-id="379c8-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="379c8-110">*Пиндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="379c8-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="379c8-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="379c8-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="379c8-112">Указатель на индекс анимации.</span><span class="sxs-lookup"><span data-stu-id="379c8-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="379c8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="379c8-113">Return value</span></span>

<span data-ttu-id="379c8-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="379c8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="379c8-115">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="379c8-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="379c8-116">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="379c8-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="379c8-117">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="379c8-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="379c8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="379c8-118">Requirements</span></span>



| <span data-ttu-id="379c8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="379c8-119">Requirement</span></span> | <span data-ttu-id="379c8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="379c8-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="379c8-121">Header</span><span class="sxs-lookup"><span data-stu-id="379c8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="379c8-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="379c8-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="379c8-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="379c8-123">Library</span></span><br/> | <dl> <span data-ttu-id="379c8-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="379c8-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="379c8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="379c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="379c8-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="379c8-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
