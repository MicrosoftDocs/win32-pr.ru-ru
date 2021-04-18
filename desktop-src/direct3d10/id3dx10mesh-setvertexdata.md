---
description: Установите данные вершин в один из буферов вершин сетки.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'Метод ID3DX10Mesh:: Сетвертексдата (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694232"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="ede15-103">Метод ID3DX10Mesh:: Сетвертексдата</span><span class="sxs-lookup"><span data-stu-id="ede15-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="ede15-104">Установите данные вершин в один из буферов вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="ede15-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede15-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ede15-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="ede15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ede15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede15-107">*iBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ede15-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede15-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ede15-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ede15-109">Буфер вершин, заполняемый с помощью pData.</span><span class="sxs-lookup"><span data-stu-id="ede15-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="ede15-110">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ede15-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede15-111">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="ede15-111">Type: **const void\***</span></span>

<span data-ttu-id="ede15-112">Устанавливаемые данные вершин.</span><span class="sxs-lookup"><span data-stu-id="ede15-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede15-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ede15-113">Return value</span></span>

<span data-ttu-id="ede15-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ede15-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ede15-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ede15-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ede15-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ede15-116">Requirements</span></span>



| <span data-ttu-id="ede15-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ede15-117">Requirement</span></span> | <span data-ttu-id="ede15-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ede15-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ede15-119">Header</span><span class="sxs-lookup"><span data-stu-id="ede15-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ede15-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ede15-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ede15-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ede15-121">Library</span></span><br/> | <dl> <span data-ttu-id="ede15-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ede15-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede15-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ede15-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede15-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ede15-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ede15-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ede15-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
