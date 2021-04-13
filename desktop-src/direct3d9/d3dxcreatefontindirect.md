---
description: Создает объект шрифта косвенно для устройства и шрифта.
ms.assetid: 480f3012-8495-47ca-a649-11ce53cee06c
title: Функция D3DXCreateFontIndirect (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateFontIndirect
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 086f9cb4cff7666fc3977551e2c9fd4a61150d46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355460"
---
# <a name="d3dxcreatefontindirect-function"></a><span data-ttu-id="ef244-103">Функция D3DXCreateFontIndirect</span><span class="sxs-lookup"><span data-stu-id="ef244-103">D3DXCreateFontIndirect function</span></span>

<span data-ttu-id="ef244-104">Создает объект шрифта косвенно для устройства и шрифта.</span><span class="sxs-lookup"><span data-stu-id="ef244-104">Creates a font object indirectly for both a device and a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef244-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef244-105">Syntax</span></span>


```C++
HRESULT D3DXCreateFontIndirect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_  const D3DXFONT_DESC     *pDesc,
  _Out_       LPD3DXFONT        *ppFont
);
```



## <a name="parameters"></a><span data-ttu-id="ef244-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef244-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef244-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef244-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ef244-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ef244-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , устройство, связываемое с объектом Font.</span><span class="sxs-lookup"><span data-stu-id="ef244-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the font object.</span></span>

</dd> <dt>

<span data-ttu-id="ef244-110">*пдеск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ef244-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef244-111">Тип: **const [**D3DXFONT \_ DESC**](d3dxfont-desc.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef244-111">Type: **const [**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="ef244-112">Указатель на структуру [**\_ DESC D3DXFONT**](d3dxfont-desc.md) , описывающую атрибуты создаваемого объекта Font.</span><span class="sxs-lookup"><span data-stu-id="ef244-112">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure, describing the attributes of the font object to create.</span></span> <span data-ttu-id="ef244-113">Если для параметров компилятора требуется Юникод, тип данных D3DXFONT \_ DESC разрешается в D3DXFONT \_ дескв; в противном случае тип данных разрешается в D3DXFONT \_ DESC.</span><span class="sxs-lookup"><span data-stu-id="ef244-113">If the compiler settings require Unicode, the data type D3DXFONT\_DESC resolves to D3DXFONT\_DESCW; otherwise, the data type resolves to D3DXFONT\_DESCA.</span></span> <span data-ttu-id="ef244-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="ef244-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ef244-115">*ппфонт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef244-115">*ppFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef244-116">Тип: **[ **LPD3DXFONT**](id3dxfont.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef244-116">Type: **[**LPD3DXFONT**](id3dxfont.md)\***</span></span>

<span data-ttu-id="ef244-117">Возвращает указатель на интерфейс [**ID3DXFont**](id3dxfont.md) , представляющий созданный объект Font.</span><span class="sxs-lookup"><span data-stu-id="ef244-117">Returns a pointer to an [**ID3DXFont**](id3dxfont.md) interface, representing the created font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef244-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef244-118">Return value</span></span>

<span data-ttu-id="ef244-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef244-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef244-120">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ef244-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ef244-121">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ef244-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef244-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef244-122">Remarks</span></span>

<span data-ttu-id="ef244-123">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="ef244-123">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ef244-124">Если определен Юникод, вызов функции разрешается в D3DXCreateFontIndirectW.</span><span class="sxs-lookup"><span data-stu-id="ef244-124">If Unicode is defined, the function call resolves to D3DXCreateFontIndirectW.</span></span> <span data-ttu-id="ef244-125">В противном случае вызов функции разрешается в D3DXCreateFontIndirectA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef244-125">Otherwise, the function call resolves to D3DXCreateFontIndirectA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef244-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ef244-126">Requirements</span></span>



| <span data-ttu-id="ef244-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ef244-127">Requirement</span></span> | <span data-ttu-id="ef244-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ef244-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef244-129">Header</span><span class="sxs-lookup"><span data-stu-id="ef244-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ef244-130"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef244-130"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ef244-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef244-131">Library</span></span><br/> | <dl> <span data-ttu-id="ef244-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef244-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef244-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef244-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef244-134">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="ef244-134">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
