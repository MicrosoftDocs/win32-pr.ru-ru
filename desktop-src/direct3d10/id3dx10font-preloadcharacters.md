---
description: Загрузка последовательности символов в видеопамять для повышения эффективности отрисовки на устройстве.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: 'ID3DX10Font: метод:P Релоадчарактерс (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664977"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="76f03-103">ID3DX10Font: метод:P Релоадчарактерс</span><span class="sxs-lookup"><span data-stu-id="76f03-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="76f03-104">Загрузка последовательности символов в видеопамять для повышения эффективности отрисовки на устройстве.</span><span class="sxs-lookup"><span data-stu-id="76f03-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f03-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76f03-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="76f03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76f03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76f03-107">*Сначала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76f03-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f03-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76f03-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76f03-109">Идентификатор первого символа, загружаемого в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="76f03-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="76f03-110">*Последний раз* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="76f03-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76f03-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76f03-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76f03-112">Идентификатор последнего символа, который должен быть загружен в видеопамять.</span><span class="sxs-lookup"><span data-stu-id="76f03-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76f03-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76f03-113">Return value</span></span>

<span data-ttu-id="76f03-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76f03-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76f03-115">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="76f03-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="76f03-116">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="76f03-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="76f03-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76f03-117">Remarks</span></span>

<span data-ttu-id="76f03-118">Этот метод создает текстуры, содержащие глифы, представляющие входные символы.</span><span class="sxs-lookup"><span data-stu-id="76f03-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="76f03-119">Глифы рисуются в виде ряда треугольников.</span><span class="sxs-lookup"><span data-stu-id="76f03-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="76f03-120">Символы не будут подготавливаться к просмотру на устройстве; ID3DX10Font: для отрисовки символов необходимо по-прежнему вызывать метод:D Равтекст.</span><span class="sxs-lookup"><span data-stu-id="76f03-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="76f03-121">Однако предварительная загрузка символов в видеопамять ID3DX10Font::D Равтекст будет использовать значительно меньше ресурсов ЦП.</span><span class="sxs-lookup"><span data-stu-id="76f03-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="76f03-122">Этот метод внутренне преобразует символы в глифы с помощью функции GDI [жетчарактерплацемент](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76f03-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="76f03-123">Требования</span><span class="sxs-lookup"><span data-stu-id="76f03-123">Requirements</span></span>



| <span data-ttu-id="76f03-124">Требование</span><span class="sxs-lookup"><span data-stu-id="76f03-124">Requirement</span></span> | <span data-ttu-id="76f03-125">Значение</span><span class="sxs-lookup"><span data-stu-id="76f03-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76f03-126">Header</span><span class="sxs-lookup"><span data-stu-id="76f03-126">Header</span></span><br/>  | <dl> <span data-ttu-id="76f03-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="76f03-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="76f03-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="76f03-128">Library</span></span><br/> | <dl> <span data-ttu-id="76f03-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76f03-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76f03-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76f03-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f03-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="76f03-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="76f03-132">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="76f03-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
