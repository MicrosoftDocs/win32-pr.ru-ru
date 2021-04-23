---
description: Проверяет параметры создания текстуры тома.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: Функция D3DXCheckVolumeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424421"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="83dff-103">Функция D3DXCheckVolumeTextureRequirements</span><span class="sxs-lookup"><span data-stu-id="83dff-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="83dff-104">Проверяет параметры создания текстуры тома.</span><span class="sxs-lookup"><span data-stu-id="83dff-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="83dff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83dff-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="83dff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83dff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83dff-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83dff-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="83dff-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="83dff-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, которое должно быть связано с текстурой тома.</span><span class="sxs-lookup"><span data-stu-id="83dff-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-110">*пвидс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="83dff-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83dff-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83dff-112">Указатель на запрошенную ширину в пикселях или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="83dff-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="83dff-113">Возвращает исправленный размер.</span><span class="sxs-lookup"><span data-stu-id="83dff-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-114">*феигхт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="83dff-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-115">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83dff-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83dff-116">Указатель на запрошенную высоту в пикселях или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="83dff-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="83dff-117">Возвращает исправленный размер.</span><span class="sxs-lookup"><span data-stu-id="83dff-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-118">*пдепс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="83dff-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-119">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83dff-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83dff-120">Указатель на запрошенную глубину в пикселях или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="83dff-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="83dff-121">Возвращает исправленный размер.</span><span class="sxs-lookup"><span data-stu-id="83dff-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-122">*пнуммиплевелс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="83dff-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-123">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="83dff-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="83dff-124">Указатель на число запрошенных mipmap уровней или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="83dff-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="83dff-125">Возвращает исправленное число уровней mipmap.</span><span class="sxs-lookup"><span data-stu-id="83dff-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-126">*Использование* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83dff-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-127">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83dff-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83dff-128">В настоящее время не используется, установите значение 0.</span><span class="sxs-lookup"><span data-stu-id="83dff-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-129">*пформат* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="83dff-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-130">Тип: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="83dff-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="83dff-131">Указатель на член перечисляемого типа [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="83dff-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="83dff-132">Указывает требуемый формат пикселей или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="83dff-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="83dff-133">Возвращает исправленный формат.</span><span class="sxs-lookup"><span data-stu-id="83dff-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="83dff-134">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83dff-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83dff-135">Тип: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="83dff-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="83dff-136">Член перечислимого типа [**D3DPOOL**](./d3dpool.md) , описывающий класс памяти, в который должна быть размещена текстура тома.</span><span class="sxs-lookup"><span data-stu-id="83dff-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83dff-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83dff-137">Return value</span></span>

<span data-ttu-id="83dff-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83dff-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83dff-139">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="83dff-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83dff-140">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ NOTAVAILABLE, D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="83dff-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="83dff-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83dff-141">Remarks</span></span>

<span data-ttu-id="83dff-142">Если параметры для этой функции недопустимы, эта функция возвращает исправленные параметры.</span><span class="sxs-lookup"><span data-stu-id="83dff-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="83dff-143">Требования</span><span class="sxs-lookup"><span data-stu-id="83dff-143">Requirements</span></span>



| <span data-ttu-id="83dff-144">Требование</span><span class="sxs-lookup"><span data-stu-id="83dff-144">Requirement</span></span> | <span data-ttu-id="83dff-145">Значение</span><span class="sxs-lookup"><span data-stu-id="83dff-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83dff-146">Header</span><span class="sxs-lookup"><span data-stu-id="83dff-146">Header</span></span><br/>  | <dl> <span data-ttu-id="83dff-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="83dff-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="83dff-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="83dff-148">Library</span></span><br/> | <dl> <span data-ttu-id="83dff-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83dff-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="83dff-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83dff-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83dff-151">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="83dff-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
