---
description: Определяет атрибуты шрифта.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Структура D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647835"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="688e6-103">D3DX10 \_ \_ структура шрифта</span><span class="sxs-lookup"><span data-stu-id="688e6-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="688e6-104">Определяет атрибуты шрифта.</span><span class="sxs-lookup"><span data-stu-id="688e6-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="688e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="688e6-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="688e6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="688e6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="688e6-107">**Height**</span><span class="sxs-lookup"><span data-stu-id="688e6-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-108">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-109">Высота в логических единицах символьной ячейки или символа шрифта.</span><span class="sxs-lookup"><span data-stu-id="688e6-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-110">**Width**</span><span class="sxs-lookup"><span data-stu-id="688e6-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-112">Ширина (в логических единицах) символов в шрифте.</span><span class="sxs-lookup"><span data-stu-id="688e6-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="688e6-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-115">Вес шрифта в диапазоне от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="688e6-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-116">**миплевелс**</span><span class="sxs-lookup"><span data-stu-id="688e6-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-118">Число запрошенных уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="688e6-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="688e6-119">Если это значение равно нулю или D3DX \_ по умолчанию, создается полная цепочка mipmap.</span><span class="sxs-lookup"><span data-stu-id="688e6-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="688e6-120">Если значение равно 1, пространство текстуры сопоставляется с пространством экрана одинаково.</span><span class="sxs-lookup"><span data-stu-id="688e6-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-121">**Наклонный**</span><span class="sxs-lookup"><span data-stu-id="688e6-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-122">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-123">Задайте значение **true** для курсивного шрифта.</span><span class="sxs-lookup"><span data-stu-id="688e6-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="688e6-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-125">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-126">Кодировка.</span><span class="sxs-lookup"><span data-stu-id="688e6-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-127">**аутпутпреЦисион**</span><span class="sxs-lookup"><span data-stu-id="688e6-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-128">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-129">Точность вывода.</span><span class="sxs-lookup"><span data-stu-id="688e6-129">Output precision.</span></span> <span data-ttu-id="688e6-130">Точность вывода определяет, насколько близко выходные данные должны соответствовать запрошенной высоте, ширине, ориентации символов, Escape, тону и типу шрифта.</span><span class="sxs-lookup"><span data-stu-id="688e6-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-131">**Качество**</span><span class="sxs-lookup"><span data-stu-id="688e6-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-132">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-133">Качество вывода.</span><span class="sxs-lookup"><span data-stu-id="688e6-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-134">**питчандфамили**</span><span class="sxs-lookup"><span data-stu-id="688e6-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-135">Тип: **[ **Byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="688e6-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-136">Высота и семейство шрифта.</span><span class="sxs-lookup"><span data-stu-id="688e6-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="688e6-137">**Преимущственно \[ LF \_ фацесизе\]**</span><span class="sxs-lookup"><span data-stu-id="688e6-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="688e6-138">Тип: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="688e6-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="688e6-139">Строка, завершающаяся нулем, которая указывает имя гарнитуры шрифта.</span><span class="sxs-lookup"><span data-stu-id="688e6-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="688e6-140">Длина строки не должна превышать 32 символов, включая завершающий символ **null** .</span><span class="sxs-lookup"><span data-stu-id="688e6-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="688e6-141">Если преимущственно является пустой строкой, будет использоваться первый шрифт, соответствующий другим указанным атрибутам.</span><span class="sxs-lookup"><span data-stu-id="688e6-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="688e6-142">Если для параметров компилятора требуется Юникод, то тип данных TCHAR разрешается в WCHAR; в противном случае тип данных разрешается в CHAR.</span><span class="sxs-lookup"><span data-stu-id="688e6-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="688e6-143">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="688e6-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="688e6-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="688e6-144">Remarks</span></span>

<span data-ttu-id="688e6-145">Параметр компилятора также определяет тип структуры.</span><span class="sxs-lookup"><span data-stu-id="688e6-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="688e6-146">Если задано значение Unicode, \_ \_ тип структуры D3DX10 Font DESC разрешается в D3DX10 \_ шрифт \_ дескв; в противном случае тип структуры разрешается в D3DX10 \_ Font \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="688e6-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="688e6-147">Возможные значения приведенных выше элементов приведены в структуре GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="688e6-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="688e6-148">Требования</span><span class="sxs-lookup"><span data-stu-id="688e6-148">Requirements</span></span>



| <span data-ttu-id="688e6-149">Требование</span><span class="sxs-lookup"><span data-stu-id="688e6-149">Requirement</span></span> | <span data-ttu-id="688e6-150">Значение</span><span class="sxs-lookup"><span data-stu-id="688e6-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="688e6-151">Header</span><span class="sxs-lookup"><span data-stu-id="688e6-151">Header</span></span><br/> | <dl> <span data-ttu-id="688e6-152"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="688e6-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="688e6-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="688e6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688e6-154">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="688e6-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
