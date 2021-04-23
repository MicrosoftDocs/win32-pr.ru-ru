---
description: Доступ к буферу атрибутов сетки.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: 'Метод ID3DX10Mesh:: Жетаттрибутебуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 161711cd28dae790fd25ff8dd192945a366e9dd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703896"
---
# <a name="id3dx10meshgetattributebuffer-method"></a><span data-ttu-id="ef33a-103">Метод ID3DX10Mesh:: Жетаттрибутебуффер</span><span class="sxs-lookup"><span data-stu-id="ef33a-103">ID3DX10Mesh::GetAttributeBuffer method</span></span>

<span data-ttu-id="ef33a-104">Доступ к буферу атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="ef33a-104">Access the mesh's attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef33a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef33a-105">Syntax</span></span>


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ef33a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef33a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef33a-107">*ппаттрибутебуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef33a-107">*ppAttributeBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef33a-108">Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ef33a-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="ef33a-109">Буфер атрибута.</span><span class="sxs-lookup"><span data-stu-id="ef33a-109">The attribute buffer.</span></span> <span data-ttu-id="ef33a-110">См. [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="ef33a-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef33a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef33a-111">Return value</span></span>

<span data-ttu-id="ef33a-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef33a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef33a-113">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ef33a-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef33a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ef33a-114">Requirements</span></span>



| <span data-ttu-id="ef33a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ef33a-115">Requirement</span></span> | <span data-ttu-id="ef33a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ef33a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef33a-117">Header</span><span class="sxs-lookup"><span data-stu-id="ef33a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ef33a-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef33a-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef33a-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef33a-119">Library</span></span><br/> | <dl> <span data-ttu-id="ef33a-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef33a-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef33a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef33a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef33a-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ef33a-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ef33a-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ef33a-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




