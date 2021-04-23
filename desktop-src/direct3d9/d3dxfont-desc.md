---
description: Определяет атрибуты шрифта.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Структура D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720891"
---
# <a name="d3dxfont_desc-structure"></a><span data-ttu-id="87103-103">\_Структура D3DXFONT DESC</span><span class="sxs-lookup"><span data-stu-id="87103-103">D3DXFONT\_DESC structure</span></span>

<span data-ttu-id="87103-104">Определяет атрибуты шрифта.</span><span class="sxs-lookup"><span data-stu-id="87103-104">Defines the attributes of a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="87103-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87103-105">Syntax</span></span>


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a><span data-ttu-id="87103-106">Члены</span><span class="sxs-lookup"><span data-stu-id="87103-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="87103-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="87103-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="87103-108">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-109">Высота в логических единицах символьной ячейки или символа шрифта.</span><span class="sxs-lookup"><span data-stu-id="87103-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="87103-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="87103-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="87103-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-112">Ширина (в логических единицах) символов в шрифте.</span><span class="sxs-lookup"><span data-stu-id="87103-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="87103-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="87103-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="87103-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-115">Вес шрифта в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="87103-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="87103-116">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="87103-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="87103-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-118">Число запрошенных уровней MIP.</span><span class="sxs-lookup"><span data-stu-id="87103-118">Number of mip levels requested.</span></span> <span data-ttu-id="87103-119">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="87103-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="87103-120">Если значение равно 1, пространство текстуры сопоставляется с пространством экрана одинаково.</span><span class="sxs-lookup"><span data-stu-id="87103-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="87103-121">**Наклонный**</span><span class="sxs-lookup"><span data-stu-id="87103-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="87103-122">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-123">Задайте значение **true** для курсивного шрифта.</span><span class="sxs-lookup"><span data-stu-id="87103-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="87103-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="87103-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="87103-125">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-126">Кодировка.</span><span class="sxs-lookup"><span data-stu-id="87103-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="87103-127">**аутпутпреЦисион**</span><span class="sxs-lookup"><span data-stu-id="87103-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="87103-128">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-129">Точность вывода.</span><span class="sxs-lookup"><span data-stu-id="87103-129">Output precision.</span></span> <span data-ttu-id="87103-130">Точность вывода определяет, насколько близко выходные данные должны соответствовать запрошенной высоте, ширине, ориентации символов, Escape, тону и типу шрифта.</span><span class="sxs-lookup"><span data-stu-id="87103-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="87103-131">**Качество**</span><span class="sxs-lookup"><span data-stu-id="87103-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="87103-132">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-133">Качество вывода.</span><span class="sxs-lookup"><span data-stu-id="87103-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="87103-134">**питчандфамили**</span><span class="sxs-lookup"><span data-stu-id="87103-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="87103-135">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87103-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87103-136">Высота и семейство шрифта.</span><span class="sxs-lookup"><span data-stu-id="87103-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="87103-137">**Преимущственно**</span><span class="sxs-lookup"><span data-stu-id="87103-137">**FaceName**</span></span>
</dt> <dd>

<span data-ttu-id="87103-138">Тип: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="87103-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="87103-139">Строка или символы, заканчивающиеся нулем и указывающие гарнитуру шрифта.</span><span class="sxs-lookup"><span data-stu-id="87103-139">A null-terminated string or characters that specifies the typeface name of the font.</span></span> <span data-ttu-id="87103-140">Длина строки не должна превышать 32 символов, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="87103-140">The length of the string must not exceed 32 characters, including the terminating null character.</span></span> <span data-ttu-id="87103-141">Если преимущственно является пустой строкой, будет использоваться первый шрифт, соответствующий другим указанным атрибутам.</span><span class="sxs-lookup"><span data-stu-id="87103-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="87103-142">Если для параметров компилятора требуется Юникод, то тип данных TCHAR разрешается в WCHAR; в противном случае тип данных разрешается в CHAR.</span><span class="sxs-lookup"><span data-stu-id="87103-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="87103-143">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="87103-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87103-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87103-144">Remarks</span></span>

<span data-ttu-id="87103-145">Параметр компилятора также определяет тип структуры.</span><span class="sxs-lookup"><span data-stu-id="87103-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="87103-146">Если определен Юникод, \_ тип структуры D3DXFONT DESC разрешается в D3DXFONT \_ дескв; в противном случае тип структуры разрешается в D3DXFONT \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="87103-146">If Unicode is defined, the D3DXFONT\_DESC structure type resolves to a D3DXFONT\_DESCW; otherwise the structure type resolves to a D3DXFONT\_DESCA.</span></span>

<span data-ttu-id="87103-147">Возможные значения приведенных выше элементов приведены в структуре GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="87103-147">Possible values of the above members are given in the GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="87103-148">Требования</span><span class="sxs-lookup"><span data-stu-id="87103-148">Requirements</span></span>



| <span data-ttu-id="87103-149">Требование</span><span class="sxs-lookup"><span data-stu-id="87103-149">Requirement</span></span> | <span data-ttu-id="87103-150">Значение</span><span class="sxs-lookup"><span data-stu-id="87103-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87103-151">Header</span><span class="sxs-lookup"><span data-stu-id="87103-151">Header</span></span><br/> | <dl> <span data-ttu-id="87103-152"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="87103-152"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87103-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87103-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87103-154">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="87103-154">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="87103-155">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="87103-155">**GetDesc**</span></span>](id3dxfont--getdesc.md)
</dt> </dl>

 

 
