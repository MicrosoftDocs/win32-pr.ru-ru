---
description: Фильтрует mipmap уровни текстуры.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Функция D3DXFilterTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713691"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="7cda8-103">Функция D3DXFilterTexture</span><span class="sxs-lookup"><span data-stu-id="7cda8-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="7cda8-104">Фильтрует mipmap уровни текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cda8-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cda8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cda8-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="7cda8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7cda8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cda8-107">*пбасетекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cda8-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cda8-108">Тип: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="7cda8-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="7cda8-109">Указатель на интерфейс [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) , представляющий объект текстуры для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7cda8-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="7cda8-110">*ппалетте* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7cda8-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cda8-111">Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="7cda8-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7cda8-112">Указатель на структуру [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , которая представляет цветовую палитру 256 для заполнения, или **значение NULL** для форматов нонпалеттизед.</span><span class="sxs-lookup"><span data-stu-id="7cda8-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="7cda8-113">Если палитра не указана, предоставляется палитра Direct3D по умолчанию (вся непрозрачная белая палитра).</span><span class="sxs-lookup"><span data-stu-id="7cda8-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="7cda8-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="7cda8-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7cda8-115">*Срклевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cda8-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cda8-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cda8-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cda8-117">Уровень, изображение которого используется для создания последующих уровней.</span><span class="sxs-lookup"><span data-stu-id="7cda8-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="7cda8-118">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию значения 0.</span><span class="sxs-lookup"><span data-stu-id="7cda8-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="7cda8-119">*Мипфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7cda8-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cda8-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7cda8-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7cda8-121">Сочетание одного или нескольких [ \_ фильтров D3DX](d3dx-filter.md) , управляющих фильтрацией mipmap.</span><span class="sxs-lookup"><span data-stu-id="7cda8-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="7cda8-122">Указание D3DX \_ по умолчанию для этого параметра эквивалентно указанию \_ поля фильтра D3DX \_ , если размер текстуры является степенью числа 2, а \_ D3DX \_ поле \| фильтра \_ D3DX \_ — в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7cda8-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cda8-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7cda8-123">Return value</span></span>

<span data-ttu-id="7cda8-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7cda8-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7cda8-125">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7cda8-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7cda8-126">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="7cda8-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cda8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7cda8-127">Remarks</span></span>

<span data-ttu-id="7cda8-128">Фильтр рекурсивно применяется к каждому уровню текстуры для создания следующего уровня текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cda8-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="7cda8-129">Запись в текстуру без выравнивания на поверхности текстуры не приведет к обновлению «грязного» прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="7cda8-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="7cda8-130">Если вызывается **D3DXFilterTexture** и поверхность не была изменена (это маловероятно в нормальных сценариях использования), приложению необходимо явно вызвать [**адддиртирект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) для текстуры.</span><span class="sxs-lookup"><span data-stu-id="7cda8-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="7cda8-131">Текстуры, созданные в пуле по умолчанию (D3DPOOL \_ по умолчанию), нельзя использовать с **D3DXFilterTexture** (если только не создан с \_ динамическим D3DUSAGE), так как для объекта требуется операция блокировки.</span><span class="sxs-lookup"><span data-stu-id="7cda8-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="7cda8-132">Обратите внимание, что блокировки в пуле по умолчанию запрещены для текстур (если они не являются динамическими).</span><span class="sxs-lookup"><span data-stu-id="7cda8-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="7cda8-133">Дополнительные сведения о [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)см. в разделе пакет SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="7cda8-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="7cda8-134">Обратите внимание, что начиная с DirectX 8,0, член Пефлагс структуры **палеттинтри** не работает, как описано в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7cda8-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="7cda8-135">Теперь элемент Пефлагс является альфа-каналом для 8 – разрядных форматов палеттизед.</span><span class="sxs-lookup"><span data-stu-id="7cda8-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="7cda8-136">Существует только одна функция фильтрации текстур, но два макроса, которые вызывают этот метод.</span><span class="sxs-lookup"><span data-stu-id="7cda8-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="7cda8-137">Требования</span><span class="sxs-lookup"><span data-stu-id="7cda8-137">Requirements</span></span>



| <span data-ttu-id="7cda8-138">Требование</span><span class="sxs-lookup"><span data-stu-id="7cda8-138">Requirement</span></span> | <span data-ttu-id="7cda8-139">Значение</span><span class="sxs-lookup"><span data-stu-id="7cda8-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cda8-140">Header</span><span class="sxs-lookup"><span data-stu-id="7cda8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="7cda8-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cda8-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7cda8-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7cda8-142">Library</span></span><br/> | <dl> <span data-ttu-id="7cda8-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cda8-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7cda8-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7cda8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cda8-145">Функции текстуры в D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7cda8-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
