---
description: Создает объект buffer.
ms.assetid: 6f44fe84-3e0b-4fb8-821a-c997944fed37
title: Функция D3DXCreateBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc54813ea9947d263febcbe843702124c68ba747
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720975"
---
# <a name="d3dxcreatebuffer-function"></a><span data-ttu-id="2625e-103">Функция D3DXCreateBuffer</span><span class="sxs-lookup"><span data-stu-id="2625e-103">D3DXCreateBuffer function</span></span>

<span data-ttu-id="2625e-104">Создает объект buffer.</span><span class="sxs-lookup"><span data-stu-id="2625e-104">Creates a buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2625e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2625e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBuffer(
  _In_  DWORD        NumBytes,
  _Out_ LPD3DXBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="2625e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2625e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2625e-107">*Нумбитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2625e-107">*NumBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2625e-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2625e-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2625e-109">Размер создаваемого буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="2625e-109">Size of the buffer to create, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2625e-110">*ппбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2625e-110">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2625e-111">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2625e-111">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2625e-112">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) , представляющий созданный объект buffer.</span><span class="sxs-lookup"><span data-stu-id="2625e-112">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, representing the created buffer object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2625e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2625e-113">Return value</span></span>

<span data-ttu-id="2625e-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2625e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2625e-115">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2625e-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2625e-116">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2625e-116">If the function fails, the return value can be one of the following: E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2625e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2625e-117">Requirements</span></span>



| <span data-ttu-id="2625e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2625e-118">Requirement</span></span> | <span data-ttu-id="2625e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2625e-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2625e-120">Header</span><span class="sxs-lookup"><span data-stu-id="2625e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2625e-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2625e-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2625e-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2625e-122">Library</span></span><br/> | <dl> <span data-ttu-id="2625e-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2625e-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2625e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2625e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2625e-125">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="2625e-125">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
