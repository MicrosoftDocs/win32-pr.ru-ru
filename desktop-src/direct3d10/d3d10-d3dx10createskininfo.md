---
description: Создает пустой объект сетки обложки с помощью декларатора.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Функция D3DX10CreateSkinInfo (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a68da20c2e2e15e3b73d55ee1df70518bba46200
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685008"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="abd52-103">Функция D3DX10CreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="abd52-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="abd52-104">Создает пустой объект сетки обложки с помощью декларатора.</span><span class="sxs-lookup"><span data-stu-id="abd52-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd52-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abd52-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="abd52-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="abd52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd52-107">*ппскининфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="abd52-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd52-108">Тип: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="abd52-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="abd52-109">Адрес указателя на [**интерфейс ID3DX10SkinInfo**](id3dx10skininfo.md), представляющий созданный объект сетки обложки.</span><span class="sxs-lookup"><span data-stu-id="abd52-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd52-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abd52-110">Return value</span></span>

<span data-ttu-id="abd52-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abd52-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abd52-112">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="abd52-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="abd52-113">Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="abd52-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="abd52-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abd52-114">Remarks</span></span>

<span data-ttu-id="abd52-115">Используйте [**ID3DX10SkinInfo:: сетбонеинфлуенце**](id3dx10skininfo-setboneinfluence.md) для заполнения пустого объекта сетки обложки, возвращаемого этим методом.</span><span class="sxs-lookup"><span data-stu-id="abd52-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd52-116">Требования</span><span class="sxs-lookup"><span data-stu-id="abd52-116">Requirements</span></span>



| <span data-ttu-id="abd52-117">Требование</span><span class="sxs-lookup"><span data-stu-id="abd52-117">Requirement</span></span> | <span data-ttu-id="abd52-118">Значение</span><span class="sxs-lookup"><span data-stu-id="abd52-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abd52-119">Header</span><span class="sxs-lookup"><span data-stu-id="abd52-119">Header</span></span><br/>  | <dl> <span data-ttu-id="abd52-120"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd52-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="abd52-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="abd52-121">Library</span></span><br/> | <dl> <span data-ttu-id="abd52-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abd52-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abd52-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abd52-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd52-124">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="abd52-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="abd52-125">Функции D3DX</span><span class="sxs-lookup"><span data-stu-id="abd52-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




