---
description: Создает объект Font для устройства и шрифта. Примечание. вместо использования этой функции рекомендуется использовать DirectWrite и библиотеку Директкстк, класс Спритефонт.
ms.assetid: a0dd02f1-c512-46d3-9e83-a785ac3ad7ee
title: Функция D3DX10CreateFont (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFont
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6e5966e50c9c997085d35854868a2a7dd0455c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703850"
---
# <a name="d3dx10createfont-function"></a><span data-ttu-id="656ff-103">Функция D3DX10CreateFont</span><span class="sxs-lookup"><span data-stu-id="656ff-103">D3DX10CreateFont function</span></span>

<span data-ttu-id="656ff-104">Создает объект Font для устройства и шрифта.</span><span class="sxs-lookup"><span data-stu-id="656ff-104">Creates a font object for a device and font.</span></span>

> [!Note]  
> <span data-ttu-id="656ff-105">Вместо использования этой функции рекомендуется использовать [DirectWrite](../directwrite/direct-write-portal.md) и библиотеку [Директкстк](https://github.com/Microsoft/DirectXTK) , класс **спритефонт** .</span><span class="sxs-lookup"><span data-stu-id="656ff-105">Instead of using this function, we recommend that you use [DirectWrite](../directwrite/direct-write-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteFont** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="656ff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="656ff-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateFont(
  _In_  ID3D10Device *pDevice,
  _In_  INT          Height,
  _In_  UINT         Width,
  _In_  UINT         Weight,
  _In_  UINT         MipLevels,
  _In_  BOOL         Italic,
  _In_  UINT         CharSet,
  _In_  UINT         OutputPrecision,
  _In_  UINT         Quality,
  _In_  UINT         PitchAndFamily,
  _In_  LPCTSTR      pFaceName,
  _Out_ LPD3DX10FONT *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="656ff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="656ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656ff-108">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-109">Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="656ff-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="656ff-110">Указатель на интерфейс ID3D10Device, устройство, связываемое с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="656ff-110">Pointer to an ID3D10Device interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-111">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-111">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-112">Тип: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-113">Высота символов в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="656ff-113">The height of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-114">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-114">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-116">Ширина символов в логических единицах.</span><span class="sxs-lookup"><span data-stu-id="656ff-116">The width of the characters in logical units.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-117">*Вес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-117">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-119">Толщина гарнитуры.</span><span class="sxs-lookup"><span data-stu-id="656ff-119">Typeface weight.</span></span> <span data-ttu-id="656ff-120">Одним из примеров является полужирный.</span><span class="sxs-lookup"><span data-stu-id="656ff-120">One example is bold.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-121">*Миплевелс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-121">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-123">Число уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="656ff-123">The number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-124">*Курсив* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-124">*Italic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-125">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-125">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-126">True для курсивного шрифта; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="656ff-126">True for italic font, false otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-127">*CharSet* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-127">*CharSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-128">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-129">Кодировка шрифта.</span><span class="sxs-lookup"><span data-stu-id="656ff-129">The character set of the font.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-130">*АутпутпреЦисион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-130">*OutputPrecision* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-131">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-131">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-132">Указывает, как Windows должна пытаться сопоставить желаемые размеры шрифтов и характеристики с фактическими шрифтами.</span><span class="sxs-lookup"><span data-stu-id="656ff-132">Specifies how Windows should attempt to match the desired font sizes and characteristics with actual fonts.</span></span> <span data-ttu-id="656ff-133">Используйте OUT \_ \_ только \_ преЦис для экземпляра, чтобы всегда получать шрифт TrueType.</span><span class="sxs-lookup"><span data-stu-id="656ff-133">Use OUT\_TT\_ONLY\_PRECIS for instance, to ensure that you always get a TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-134">*Качество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-134">*Quality* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-135">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-136">Указывает, как Windows должна соответствовать желаемому шрифту с реальным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="656ff-136">Specifies how Windows should match the desired font with a real font.</span></span> <span data-ttu-id="656ff-137">Он применяется только к растровым шрифтам и не должен влиять на шрифты TrueType.</span><span class="sxs-lookup"><span data-stu-id="656ff-137">It applies to raster fonts only and should not affect TrueType fonts.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-138">*Питчандфамили* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-138">*PitchAndFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-139">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-139">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-140">Индекс по высоте и семейству.</span><span class="sxs-lookup"><span data-stu-id="656ff-140">Pitch and family index.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-141">*пфаценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="656ff-141">*pFaceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-142">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656ff-142">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656ff-143">Строка, содержащая имя гарнитуры.</span><span class="sxs-lookup"><span data-stu-id="656ff-143">String containing the typeface name.</span></span> <span data-ttu-id="656ff-144">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="656ff-144">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="656ff-145">В противном случае тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="656ff-145">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="656ff-146">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="656ff-146">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="656ff-147">*ппфонт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="656ff-147">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="656ff-148">Тип: **[ **LPD3DX10FONT**](id3dx10font.md)\***</span><span class="sxs-lookup"><span data-stu-id="656ff-148">Type: **[**LPD3DX10FONT**](id3dx10font.md)\***</span></span>

<span data-ttu-id="656ff-149">Возвращает указатель на интерфейс ID3DX10Font, представляющий созданный объект Font.</span><span class="sxs-lookup"><span data-stu-id="656ff-149">Returns a pointer to an ID3DX10Font interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656ff-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="656ff-150">Return value</span></span>

<span data-ttu-id="656ff-151">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="656ff-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="656ff-152">Если функция выполнена успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="656ff-152">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="656ff-153">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="656ff-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="656ff-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="656ff-154">Remarks</span></span>

<span data-ttu-id="656ff-155">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="656ff-155">The compiler setting also determines the function version.</span></span> <span data-ttu-id="656ff-156">Если определен Юникод, вызов функции разрешается в D3DXCreateFontW.</span><span class="sxs-lookup"><span data-stu-id="656ff-156">If Unicode is defined, the function call resolves to D3DXCreateFontW.</span></span> <span data-ttu-id="656ff-157">В противном случае вызов функции разрешается в D3DXCreateFontA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="656ff-157">Otherwise, the function call resolves to D3DXCreateFontA because ANSI strings are being used.</span></span>

<span data-ttu-id="656ff-158">Дополнительные сведения о параметрах шрифтов см. в разделе [логический шрифт](/previous-versions//ms533985(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="656ff-158">If you want more information about font parameters, see [The Logical Font](/previous-versions//ms533985(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="656ff-159">Требования</span><span class="sxs-lookup"><span data-stu-id="656ff-159">Requirements</span></span>



| <span data-ttu-id="656ff-160">Требование</span><span class="sxs-lookup"><span data-stu-id="656ff-160">Requirement</span></span> | <span data-ttu-id="656ff-161">Значение</span><span class="sxs-lookup"><span data-stu-id="656ff-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="656ff-162">Header</span><span class="sxs-lookup"><span data-stu-id="656ff-162">Header</span></span><br/>  | <dl> <span data-ttu-id="656ff-163"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="656ff-163"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="656ff-164">Библиотека</span><span class="sxs-lookup"><span data-stu-id="656ff-164">Library</span></span><br/> | <dl> <span data-ttu-id="656ff-165"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="656ff-165"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="656ff-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="656ff-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656ff-167">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="656ff-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
