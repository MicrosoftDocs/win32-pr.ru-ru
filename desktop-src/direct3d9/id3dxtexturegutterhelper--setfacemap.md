---
description: Задает индекс грани сетки, к которой принадлежит каждый шаг текселя.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'Метод ID3DXTextureGutterHelper:: Сетфацемап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273921"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="c3ad5-103">Метод ID3DXTextureGutterHelper:: Сетфацемап</span><span class="sxs-lookup"><span data-stu-id="c3ad5-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="c3ad5-104">Задает индекс грани сетки, к которой принадлежит каждый шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ad5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3ad5-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="c3ad5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3ad5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ad5-107">*пфацедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3ad5-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ad5-108">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3ad5-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3ad5-109">Указатель на индекс грани сетки, к которой принадлежит каждый шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ad5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3ad5-110">Return value</span></span>

<span data-ttu-id="c3ad5-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3ad5-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3ad5-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c3ad5-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c3ad5-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="c3ad5-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ad5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3ad5-114">Remarks</span></span>

<span data-ttu-id="c3ad5-115">Входные данные грани сетки для этого метода допустимы только для допустимых пикселей текстуры (не являющихся классами 0).</span><span class="sxs-lookup"><span data-stu-id="c3ad5-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="c3ad5-116">[**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="c3ad5-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ad5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c3ad5-117">Requirements</span></span>



| <span data-ttu-id="c3ad5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c3ad5-118">Requirement</span></span> | <span data-ttu-id="c3ad5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ad5-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ad5-120">Header</span><span class="sxs-lookup"><span data-stu-id="c3ad5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c3ad5-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ad5-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c3ad5-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3ad5-122">Library</span></span><br/> | <dl> <span data-ttu-id="c3ad5-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3ad5-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3ad5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3ad5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ad5-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="c3ad5-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
