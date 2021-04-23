---
description: Получите указатель на память буфера сетки, чтобы изменить ее содержимое.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'Метод ID3DX10MeshBuffer:: Map (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354943"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="197da-103">Метод ID3DX10MeshBuffer:: Map</span><span class="sxs-lookup"><span data-stu-id="197da-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="197da-104">Получите указатель на память буфера сетки, чтобы изменить ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="197da-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="197da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="197da-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="197da-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="197da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="197da-107">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="197da-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="197da-108">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="197da-108">Type: **void\*\***</span></span>

<span data-ttu-id="197da-109">Указатель на данные буфера.</span><span class="sxs-lookup"><span data-stu-id="197da-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="197da-110">*псизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="197da-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="197da-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="197da-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="197da-112">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="197da-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="197da-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="197da-113">Return value</span></span>

<span data-ttu-id="197da-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="197da-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="197da-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="197da-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="197da-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="197da-116">Remarks</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="197da-117">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="197da-117">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="197da-118">Map () в Direct3D 10 аналогичен карте ресурсов () в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="197da-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="197da-119">Требования</span><span class="sxs-lookup"><span data-stu-id="197da-119">Requirements</span></span>



| <span data-ttu-id="197da-120">Требование</span><span class="sxs-lookup"><span data-stu-id="197da-120">Requirement</span></span> | <span data-ttu-id="197da-121">Значение</span><span class="sxs-lookup"><span data-stu-id="197da-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="197da-122">Header</span><span class="sxs-lookup"><span data-stu-id="197da-122">Header</span></span><br/>  | <dl> <span data-ttu-id="197da-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="197da-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="197da-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="197da-124">Library</span></span><br/> | <dl> <span data-ttu-id="197da-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="197da-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="197da-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="197da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197da-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="197da-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="197da-128">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="197da-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
