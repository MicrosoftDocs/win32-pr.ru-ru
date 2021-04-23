---
description: Создает сетку, содержащую указанный текст, используя шрифт, связанный с контекстом устройства.
ms.assetid: 1c8b0dc6-51b8-45bf-b4c0-b67e3d128097
title: Функция D3DXCreateText (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateText
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f6202a534dde727e21b6513ad30077f2e3b3e52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694168"
---
# <a name="d3dxcreatetext-function"></a><span data-ttu-id="dd174-103">Функция D3DXCreateText</span><span class="sxs-lookup"><span data-stu-id="dd174-103">D3DXCreateText function</span></span>

<span data-ttu-id="dd174-104">Создает сетку, содержащую указанный текст, используя шрифт, связанный с контекстом устройства.</span><span class="sxs-lookup"><span data-stu-id="dd174-104">Creates a mesh containing the specified text, using the font associated with the device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd174-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd174-105">Syntax</span></span>


```C++
HRESULT D3DXCreateText(
  _In_  LPDIRECT3DDEVICE9   pDevice,
  _In_  HDC                 hDC,
  _In_  LPCTSTR             pText,
  _In_  FLOAT               Deviation,
  _In_  FLOAT               Extrusion,
  _Out_ LPD3DXMESH          *ppMesh,
  _Out_ LPD3DXBUFFER        *ppAdjacency,
  _Out_ LPGLYPHMETRICSFLOAT pGlyphMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="dd174-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd174-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd174-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="dd174-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="dd174-109">Указатель на устройство, создавшее сетку.</span><span class="sxs-lookup"><span data-stu-id="dd174-109">Pointer to the device that created the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-110">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd174-110">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-111">Тип: **HDC**</span><span class="sxs-lookup"><span data-stu-id="dd174-111">Type: **HDC**</span></span>

<span data-ttu-id="dd174-112">Контекст устройства, содержащий шрифт для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dd174-112">Device context, containing the font for output.</span></span> <span data-ttu-id="dd174-113">Шрифт, выбранный в контексте устройства, должен быть шрифтом TrueType.</span><span class="sxs-lookup"><span data-stu-id="dd174-113">The font selected by the device context must be a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-114">*птекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd174-114">*pText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-115">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd174-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd174-116">Указатель на строку, указывающую создаваемый текст.</span><span class="sxs-lookup"><span data-stu-id="dd174-116">Pointer to a string that specifies the text to generate.</span></span> <span data-ttu-id="dd174-117">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="dd174-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="dd174-118">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="dd174-118">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="dd174-119">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="dd174-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-120">*Отклонение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd174-120">*Deviation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-121">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd174-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd174-122">Максимальное отклонение в соответствии с контурами шрифтов TrueType.</span><span class="sxs-lookup"><span data-stu-id="dd174-122">Maximum chordal deviation from TrueType font outlines.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-123"> Объем \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd174-123">*Extrusion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-124">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd174-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dd174-125">Величина вытягивания текста в отрицательном z-направлении.</span><span class="sxs-lookup"><span data-stu-id="dd174-125">Amount to extrude text in the negative z-direction.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-126">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd174-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-127">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="dd174-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="dd174-128">Указатель на возвращенную сетку.</span><span class="sxs-lookup"><span data-stu-id="dd174-128">Pointer to the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-129">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd174-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-130">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dd174-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dd174-131">Указатель на буфер, содержащий сведения о смежности.</span><span class="sxs-lookup"><span data-stu-id="dd174-131">Pointer to a buffer containing adjacency information.</span></span> <span data-ttu-id="dd174-132">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dd174-132">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dd174-133">*пглифметрикс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dd174-133">*pGlyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd174-134">Тип: **[ **лпглифметриксфлоат**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span><span class="sxs-lookup"><span data-stu-id="dd174-134">Type: **[**LPGLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat)**</span></span>

<span data-ttu-id="dd174-135">Указатель на массив структур [**глифметриксфлоат**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) , содержащих данные метрики глифа.</span><span class="sxs-lookup"><span data-stu-id="dd174-135">Pointer to an array of [**GLYPHMETRICSFLOAT**](/windows/win32/api/wingdi/ns-wingdi-glyphmetricsfloat) structures that contain the glyph metric data.</span></span> <span data-ttu-id="dd174-136">Каждый элемент содержит сведения о положении и ориентации соответствующего глифа в строке.</span><span class="sxs-lookup"><span data-stu-id="dd174-136">Each element contains information about the position and orientation of the corresponding glyph in the string.</span></span> <span data-ttu-id="dd174-137">Число элементов в массиве должно быть равно числу символов в строке.</span><span class="sxs-lookup"><span data-stu-id="dd174-137">The number of elements in the array should be equal to the number of characters in the string.</span></span> <span data-ttu-id="dd174-138">Обратите внимание, что источник в каждой структуре не является относительным относительно всей строки, а задается относительно этой символьной ячейки.</span><span class="sxs-lookup"><span data-stu-id="dd174-138">Note that the origin in each structure is not relative to the entire string, but rather is relative to that character cell.</span></span> <span data-ttu-id="dd174-139">Чтобы вычислить весь ограничивающий прямоугольник, добавьте шаг приращения для каждого глифа во время прохода по строке.</span><span class="sxs-lookup"><span data-stu-id="dd174-139">To compute the entire bounding box, add the increment for each glyph while traversing the string.</span></span> <span data-ttu-id="dd174-140">Если вы не беспокоитесь о размере глифов, присвойте этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dd174-140">If you are not concerned with the glyph sizes, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd174-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd174-141">Return value</span></span>

<span data-ttu-id="dd174-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd174-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd174-143">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="dd174-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dd174-144">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dd174-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd174-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd174-145">Remarks</span></span>

<span data-ttu-id="dd174-146">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="dd174-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="dd174-147">Если определен Юникод, вызов функции разрешается в D3DXCreateTextW.</span><span class="sxs-lookup"><span data-stu-id="dd174-147">If Unicode is defined, the function call resolves to D3DXCreateTextW.</span></span> <span data-ttu-id="dd174-148">В противном случае вызов функции разрешается в D3DXCreateTextA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="dd174-148">Otherwise, the function call resolves to D3DXCreateTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="dd174-149">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="dd174-149">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd174-150">Требования</span><span class="sxs-lookup"><span data-stu-id="dd174-150">Requirements</span></span>



| <span data-ttu-id="dd174-151">Требование</span><span class="sxs-lookup"><span data-stu-id="dd174-151">Requirement</span></span> | <span data-ttu-id="dd174-152">Значение</span><span class="sxs-lookup"><span data-stu-id="dd174-152">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd174-153">Header</span><span class="sxs-lookup"><span data-stu-id="dd174-153">Header</span></span><br/>  | <dl> <span data-ttu-id="dd174-154"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd174-154"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="dd174-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dd174-155">Library</span></span><br/> | <dl> <span data-ttu-id="dd174-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd174-156"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dd174-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd174-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd174-158">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="dd174-158">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
