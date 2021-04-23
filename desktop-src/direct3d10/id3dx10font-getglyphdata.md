---
description: Возвращает сведения о размещении и ориентации глифа в символьной ячейке.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'Метод ID3DX10Font:: Жетглифдата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703901"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="c93ef-103">Метод ID3DX10Font:: Жетглифдата</span><span class="sxs-lookup"><span data-stu-id="c93ef-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="c93ef-104">Возвращает сведения о размещении и ориентации глифа в символьной ячейке.</span><span class="sxs-lookup"><span data-stu-id="c93ef-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c93ef-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="c93ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c93ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93ef-107">*Глиф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c93ef-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ef-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c93ef-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c93ef-109">Идентификатор глифа.</span><span class="sxs-lookup"><span data-stu-id="c93ef-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c93ef-110">*пптекстуре* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c93ef-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ef-111">Тип: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="c93ef-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="c93ef-112">Адрес указателя на объект ID3D10Texture, который содержит глиф.</span><span class="sxs-lookup"><span data-stu-id="c93ef-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="c93ef-113">*пблаккбокс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c93ef-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ef-114">Тип: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="c93ef-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="c93ef-115">Указатель на самый маленький объект Rectangle, полностью охватывающий глиф.</span><span class="sxs-lookup"><span data-stu-id="c93ef-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="c93ef-116">См. раздел [Rect](/previous-versions//ms536136(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c93ef-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c93ef-117">*пцеллинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c93ef-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c93ef-118">Тип: **точка \***</span><span class="sxs-lookup"><span data-stu-id="c93ef-118">Type: **POINT\***</span></span>

<span data-ttu-id="c93ef-119">Указатель на двухмерный вектор, соединяющий источник текущей ячейки символов с источником следующей ячейки символа.</span><span class="sxs-lookup"><span data-stu-id="c93ef-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="c93ef-120">См. раздел [Point](/previous-versions//ms536119(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c93ef-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93ef-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c93ef-121">Return value</span></span>

<span data-ttu-id="c93ef-122">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c93ef-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c93ef-123">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="c93ef-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c93ef-124">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="c93ef-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93ef-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c93ef-125">Requirements</span></span>



| <span data-ttu-id="c93ef-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c93ef-126">Requirement</span></span> | <span data-ttu-id="c93ef-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c93ef-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c93ef-128">Header</span><span class="sxs-lookup"><span data-stu-id="c93ef-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c93ef-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c93ef-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c93ef-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c93ef-130">Library</span></span><br/> | <dl> <span data-ttu-id="c93ef-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c93ef-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93ef-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c93ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93ef-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="c93ef-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="c93ef-134">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="c93ef-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
