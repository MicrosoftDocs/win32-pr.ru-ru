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
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335358"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="80035-103">Метод ID3DX10MeshBuffer:: Map</span><span class="sxs-lookup"><span data-stu-id="80035-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="80035-104">Получите указатель на память буфера сетки, чтобы изменить ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="80035-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="80035-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80035-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="80035-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80035-107">*ппдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80035-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80035-108">Тип: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="80035-108">Type: **void\*\***</span></span>

<span data-ttu-id="80035-109">Указатель на данные буфера.</span><span class="sxs-lookup"><span data-stu-id="80035-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="80035-110">*псизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80035-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80035-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="80035-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="80035-112">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="80035-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80035-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80035-113">Return value</span></span>

<span data-ttu-id="80035-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80035-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80035-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="80035-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="80035-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80035-116">Remarks</span></span>



 <span data-ttu-id="80035-117">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="80035-117">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="80035-118">Map () в Direct3D 10 аналогичен карте ресурсов () в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="80035-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="80035-119">Требования</span><span class="sxs-lookup"><span data-stu-id="80035-119">Requirements</span></span>



| <span data-ttu-id="80035-120">Требование</span><span class="sxs-lookup"><span data-stu-id="80035-120">Requirement</span></span> | <span data-ttu-id="80035-121">Значение</span><span class="sxs-lookup"><span data-stu-id="80035-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80035-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="80035-122">Header</span></span><br/>  | <dl> <span data-ttu-id="80035-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="80035-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="80035-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80035-124">Library</span></span><br/> | <dl> <span data-ttu-id="80035-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80035-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80035-126">См. также</span><span class="sxs-lookup"><span data-stu-id="80035-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80035-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="80035-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="80035-128">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="80035-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
