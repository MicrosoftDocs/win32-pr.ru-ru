---
description: Возвращает сведения о размещении и ориентации глифа в ячейке символов.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'Метод ID3DXFont:: Жетглифдата (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105685000"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="f4f0b-103">Метод ID3DXFont:: Жетглифдата</span><span class="sxs-lookup"><span data-stu-id="f4f0b-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="f4f0b-104">Возвращает сведения о размещении и ориентации глифа в ячейке символов.</span><span class="sxs-lookup"><span data-stu-id="f4f0b-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4f0b-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="f4f0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4f0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f0b-107">*Глиф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4f0b-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f0b-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4f0b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f4f0b-109">Идентификатор глифа.</span><span class="sxs-lookup"><span data-stu-id="f4f0b-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f4f0b-110">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f0b-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f0b-111">Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="f4f0b-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="f4f0b-112">Адрес указателя на объект [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , который содержит глиф.</span><span class="sxs-lookup"><span data-stu-id="f4f0b-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="f4f0b-113">*пблаккбокс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f0b-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f0b-114">Тип: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="f4f0b-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="f4f0b-115">Указатель на самый маленький объект Rectangle, полностью охватывающий глиф.</span><span class="sxs-lookup"><span data-stu-id="f4f0b-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="f4f0b-116">*пцеллинк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f0b-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f0b-117">Тип: **[ **точка**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4f0b-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f4f0b-118">Указатель на двухмерный вектор, соединяющий источник текущей ячейки символов с источником следующей ячейки символа.</span><span class="sxs-lookup"><span data-stu-id="f4f0b-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="f4f0b-119">См. раздел [**Point**](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="f4f0b-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f0b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4f0b-120">Return value</span></span>

<span data-ttu-id="f4f0b-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f4f0b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f4f0b-122">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="f4f0b-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f4f0b-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f4f0b-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f0b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f4f0b-124">Requirements</span></span>



| <span data-ttu-id="f4f0b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f4f0b-125">Requirement</span></span> | <span data-ttu-id="f4f0b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f4f0b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f0b-127">Header</span><span class="sxs-lookup"><span data-stu-id="f4f0b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f4f0b-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f0b-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f4f0b-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4f0b-129">Library</span></span><br/> | <dl> <span data-ttu-id="f4f0b-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4f0b-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f4f0b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4f0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f0b-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="f4f0b-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
