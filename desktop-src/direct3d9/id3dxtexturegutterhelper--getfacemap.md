---
description: Извлекает индекс грани сетки, к которой принадлежит каждый шаг текселя.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'Метод ID3DXTextureGutterHelper:: Жетфацемап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703855"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="1096d-103">Метод ID3DXTextureGutterHelper:: Жетфацемап</span><span class="sxs-lookup"><span data-stu-id="1096d-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="1096d-104">Извлекает индекс грани сетки, к которой принадлежит каждый шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="1096d-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1096d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1096d-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="1096d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1096d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1096d-107">*пфацедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1096d-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1096d-108">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1096d-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1096d-109">Указатель на индекс грани сетки, к которой принадлежит каждый шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="1096d-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1096d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1096d-110">Return value</span></span>

<span data-ttu-id="1096d-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1096d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1096d-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1096d-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1096d-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="1096d-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="1096d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1096d-114">Remarks</span></span>

<span data-ttu-id="1096d-115">Данные о грани сетки, возвращаемые этим методом, допустимы только для допустимых пикселей текстуры (не являющихся классами 0).</span><span class="sxs-lookup"><span data-stu-id="1096d-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="1096d-116">[**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого (не класса 0) пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="1096d-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="1096d-117">Для [**класса 2 пикселей текстуры**](id3dxtexturegutterhelper.md)этот метод извлекает ближайшее лицо.</span><span class="sxs-lookup"><span data-stu-id="1096d-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="1096d-118">Приложение должно выделить Пфацедата и управлять им.</span><span class="sxs-lookup"><span data-stu-id="1096d-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="1096d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1096d-119">Requirements</span></span>



| <span data-ttu-id="1096d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1096d-120">Requirement</span></span> | <span data-ttu-id="1096d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1096d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1096d-122">Header</span><span class="sxs-lookup"><span data-stu-id="1096d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1096d-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1096d-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1096d-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1096d-124">Library</span></span><br/> | <dl> <span data-ttu-id="1096d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1096d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1096d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1096d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1096d-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="1096d-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
