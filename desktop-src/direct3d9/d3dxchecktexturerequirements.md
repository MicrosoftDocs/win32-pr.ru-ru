---
description: Проверяет параметры создания текстуры.
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: Функция D3DXCheckTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273822"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="198ee-103">Функция D3DXCheckTextureRequirements</span><span class="sxs-lookup"><span data-stu-id="198ee-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="198ee-104">Проверяет параметры создания текстуры.</span><span class="sxs-lookup"><span data-stu-id="198ee-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="198ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="198ee-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="198ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="198ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198ee-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="198ee-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="198ee-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="198ee-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой.</span><span class="sxs-lookup"><span data-stu-id="198ee-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="198ee-110">*пвидс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="198ee-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="198ee-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="198ee-112">Указатель на запрошенную ширину в пикселях или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="198ee-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="198ee-113">Возвращает исправленный размер.</span><span class="sxs-lookup"><span data-stu-id="198ee-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="198ee-114">*феигхт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="198ee-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-115">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="198ee-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="198ee-116">Указатель на запрошенную высоту в пикселях или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="198ee-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="198ee-117">Возвращает исправленный размер.</span><span class="sxs-lookup"><span data-stu-id="198ee-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="198ee-118">*пнуммиплевелс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="198ee-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-119">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="198ee-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="198ee-120">Указатель на число запрошенных уровней mipmap или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="198ee-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="198ee-121">Возвращает исправленное число уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="198ee-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="198ee-122">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="198ee-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-123">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="198ee-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="198ee-124">0 или [**D3DUSAGE \_ рендертаржет**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="198ee-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="198ee-125">Установка этого флага в значение D3DUSAGE \_ рендертаржет указывает, что поверхность должна использоваться в качестве целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="198ee-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="198ee-126">Затем ресурс можно передать в параметр Пневрендертаржет метода [**сетрендертаржет**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="198ee-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="198ee-127">Если указан параметр **D3DUSAGE \_ рендертаржет** , приложение должно проверить, поддерживает ли устройство эту операцию, вызвав [**чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span><span class="sxs-lookup"><span data-stu-id="198ee-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="198ee-128">*пформат* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="198ee-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-129">Тип: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="198ee-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="198ee-130">Указатель на член перечисляемого типа [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="198ee-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="198ee-131">Указывает требуемый формат пикселей или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="198ee-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="198ee-132">Возвращает исправленный формат.</span><span class="sxs-lookup"><span data-stu-id="198ee-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="198ee-133">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="198ee-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="198ee-134">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="198ee-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="198ee-135">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура.</span><span class="sxs-lookup"><span data-stu-id="198ee-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198ee-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="198ee-136">Return value</span></span>

<span data-ttu-id="198ee-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="198ee-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="198ee-138">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="198ee-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="198ee-139">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="198ee-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="198ee-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="198ee-140">Remarks</span></span>

<span data-ttu-id="198ee-141">Если параметры для этой функции недопустимы, эта функция возвращает исправленные параметры.</span><span class="sxs-lookup"><span data-stu-id="198ee-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="198ee-142">Эта функция использует следующие эвристики при сравнении запрошенных требований с доступными форматами:</span><span class="sxs-lookup"><span data-stu-id="198ee-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="198ee-143">Не выбирайте формат с меньшим числом каналов.</span><span class="sxs-lookup"><span data-stu-id="198ee-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="198ee-144">Избегайте использования типов [FourCC](d3dformat.md) и 24-разрядных форматов, если они не запрошены явным образом.</span><span class="sxs-lookup"><span data-stu-id="198ee-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="198ee-145">Попробуйте не добавлять новые каналы.</span><span class="sxs-lookup"><span data-stu-id="198ee-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="198ee-146">Попробуйте не изменять число бит на канал.</span><span class="sxs-lookup"><span data-stu-id="198ee-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="198ee-147">Старайтесь не преобразовывать типы форматов.</span><span class="sxs-lookup"><span data-stu-id="198ee-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="198ee-148">Например, Избегайте преобразования формата ARGB в формат глубины.</span><span class="sxs-lookup"><span data-stu-id="198ee-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="198ee-149">Требования</span><span class="sxs-lookup"><span data-stu-id="198ee-149">Requirements</span></span>



| <span data-ttu-id="198ee-150">Требование</span><span class="sxs-lookup"><span data-stu-id="198ee-150">Requirement</span></span> | <span data-ttu-id="198ee-151">Значение</span><span class="sxs-lookup"><span data-stu-id="198ee-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="198ee-152">Header</span><span class="sxs-lookup"><span data-stu-id="198ee-152">Header</span></span><br/>  | <dl> <span data-ttu-id="198ee-153"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="198ee-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="198ee-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="198ee-154">Library</span></span><br/> | <dl> <span data-ttu-id="198ee-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="198ee-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="198ee-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="198ee-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198ee-157">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="198ee-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
