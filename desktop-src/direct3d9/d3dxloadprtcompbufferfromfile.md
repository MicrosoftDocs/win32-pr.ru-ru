---
description: Загружает в память сжатый предварительно вычисленный буфер радианценой пересылки (PRT), сохраненный на диске.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Функция D3DXLoadPRTCompBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355813"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="9b2f6-103">Функция D3DXLoadPRTCompBufferFromFile</span><span class="sxs-lookup"><span data-stu-id="9b2f6-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="9b2f6-104">Загружает в память сжатый предварительно вычисленный буфер радианценой пересылки (PRT), сохраненный на диске.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b2f6-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="9b2f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b2f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b2f6-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b2f6-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2f6-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9b2f6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9b2f6-109">Имя файла, из которого загружаются данные сжатого буфера.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="9b2f6-110">*ппбуффер* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9b2f6-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b2f6-111">Тип: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9b2f6-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="9b2f6-112">Адрес указателя на выходной объект [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9b2f6-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b2f6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b2f6-113">Return value</span></span>

<span data-ttu-id="9b2f6-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9b2f6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9b2f6-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9b2f6-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b2f6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b2f6-117">Remarks</span></span>

<span data-ttu-id="9b2f6-118">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9b2f6-119">Если определен Юникод, вызов функции разрешается в D3DXLoadPRTCompBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="9b2f6-120">В противном случае вызов функции разрешается в D3DXLoadPRTCompBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="9b2f6-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2f6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9b2f6-121">Requirements</span></span>



| <span data-ttu-id="9b2f6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9b2f6-122">Requirement</span></span> | <span data-ttu-id="9b2f6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9b2f6-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2f6-124">Header</span><span class="sxs-lookup"><span data-stu-id="9b2f6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9b2f6-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b2f6-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9b2f6-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b2f6-126">Library</span></span><br/> | <dl> <span data-ttu-id="9b2f6-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b2f6-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b2f6-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b2f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b2f6-129">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="9b2f6-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
