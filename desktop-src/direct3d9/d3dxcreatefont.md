---
description: Создает объект Font для устройства и шрифта.
ms.assetid: 3e65dfdc-9608-420c-9672-c38289d13ab1
title: Функция D3DXCreateFont (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFont
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488a400928ecc270612a307fbede971e02b43b25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821277"
---
# <a name="d3dxcreatefont-function"></a><span data-ttu-id="0421a-103">Функция D3DXCreateFont</span><span class="sxs-lookup"><span data-stu-id="0421a-103">D3DXCreateFont function</span></span>

<span data-ttu-id="0421a-104">Создает объект Font для устройства и шрифта.</span><span class="sxs-lookup"><span data-stu-id="0421a-104">Creates a font object for a device and font.</span></span>

## <a name="syntax"></a><span data-ttu-id="0421a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0421a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFont(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  INT               Height,
  _In_  UINT              Width,
  _In_  UINT              Weight,
  _In_  UINT              MipLevels,
  _In_  BOOL              Italic,
  _In_  DWORD             CharSet,
  _In_  DWORD             OutputPrecision,
  _In_  DWORD             Quality,
  _In_  DWORD             PitchAndFamily,
  _In_  LPCTSTR           pFacename,
  _Out_ LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="0421a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0421a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0421a-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0421a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0421a-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, связываемое с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="0421a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-110">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-111">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-111">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-112">Высота символов в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="0421a-112">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-113">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-113">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-115">Ширина символов в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="0421a-115">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-116">*Вес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-116">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-118">Толщина гарнитуры.</span><span class="sxs-lookup"><span data-stu-id="0421a-118">Typeface weight.</span></span> <span data-ttu-id="0421a-119">Одним из примеров является полужирный.</span><span class="sxs-lookup"><span data-stu-id="0421a-119">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-120">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-121">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-122">Число уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="0421a-122">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-123">*Курсив* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-123">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-124">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-124">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-125">True для курсивного шрифта; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="0421a-125">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-126">*CharSet* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-126">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-128">Кодировка шрифта.</span><span class="sxs-lookup"><span data-stu-id="0421a-128">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-129">*АутпутпреЦисион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-129">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-130">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-131">Указывает, как Windows должна пытаться сопоставить желаемые размеры шрифтов и характеристики с фактическими шрифтами.</span><span class="sxs-lookup"><span data-stu-id="0421a-131">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="0421a-132">Используйте OUT \_ \_ только \_ преЦис для экземпляра, чтобы всегда получать шрифт TrueType.</span><span class="sxs-lookup"><span data-stu-id="0421a-132">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-133">*Качество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-133">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-135">Указывает, как Windows должна соответствовать желаемому шрифту с реальным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="0421a-135">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="0421a-136">Он применяется только к растровым шрифтам и не должен влиять на шрифты TrueType.</span><span class="sxs-lookup"><span data-stu-id="0421a-136">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-137">*Питчандфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-137">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-138">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-139">Индекс по высоте и семейству.</span><span class="sxs-lookup"><span data-stu-id="0421a-139">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-140">*пфаценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0421a-140">*pFacename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-141">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0421a-141">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0421a-142">Строка, содержащая имя гарнитуры.</span><span class="sxs-lookup"><span data-stu-id="0421a-142">String containing the typeface name.</span></span> <span data-ttu-id="0421a-143">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="0421a-143">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0421a-144">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="0421a-144">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="0421a-145">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="0421a-145">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0421a-146">*ппфонт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0421a-146">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0421a-147">Тип: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="0421a-147">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="0421a-148">Возвращает указатель на интерфейс [**ID3DXFont**](id3dxfont.md) , представляющий созданный объект Font.</span><span class="sxs-lookup"><span data-stu-id="0421a-148">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0421a-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0421a-149">Return value</span></span>

<span data-ttu-id="0421a-150">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0421a-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0421a-151">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0421a-151">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0421a-152">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0421a-152">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0421a-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0421a-153">Remarks</span></span>

<span data-ttu-id="0421a-154">Для создания объекта ID3DXFont требуется, чтобы устройство поддерживало 32-разрядный цвет.</span><span class="sxs-lookup"><span data-stu-id="0421a-154">The creation of an ID3DXFont object requires that the device supports 32-bit color.</span></span>

<span data-ttu-id="0421a-155">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="0421a-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0421a-156">Если определен Юникод, вызов функции разрешается в D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="0421a-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="0421a-157">В противном случае вызов функции разрешается в D3DXCreateFontA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="0421a-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="0421a-158">Дополнительные сведения о параметрах шрифтов см. в разделе [логический шрифт](../gdi/creating-a-logical-font.md).</span><span class="sxs-lookup"><span data-stu-id="0421a-158">If you want more information about font parameters, see [The Logical Font](../gdi/creating-a-logical-font.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0421a-159">Требования</span><span class="sxs-lookup"><span data-stu-id="0421a-159">Requirements</span></span>



| <span data-ttu-id="0421a-160">Требование</span><span class="sxs-lookup"><span data-stu-id="0421a-160">Requirement</span></span> | <span data-ttu-id="0421a-161">Значение</span><span class="sxs-lookup"><span data-stu-id="0421a-161">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0421a-162">Header</span><span class="sxs-lookup"><span data-stu-id="0421a-162">Header</span></span><br/>  | <dl> <span data-ttu-id="0421a-163"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0421a-163"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="0421a-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0421a-164">Library</span></span><br/> | <dl> <span data-ttu-id="0421a-165"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0421a-165"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0421a-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0421a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0421a-167">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="0421a-167">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
