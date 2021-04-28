---
description: 'Метод ID3DX10Mesh:: Жетиндексбуффер — получает данные в буфере индекса.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'Метод ID3DX10Mesh:: Жетиндексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 751d6dd0376dc73f0213ddb83a19954dc154d633
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084032"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="7f089-103">Метод ID3DX10Mesh:: Жетиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="7f089-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="7f089-104">Получает данные в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="7f089-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f089-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f089-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="7f089-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f089-107">*ппиндексбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f089-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f089-108">Тип: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7f089-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="7f089-109">Адрес указателя на интерфейс ID3DX10MeshBuffer, представляющий буфер индекса, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="7f089-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f089-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f089-110">Return value</span></span>

<span data-ttu-id="7f089-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f089-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f089-112">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7f089-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f089-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7f089-113">Requirements</span></span>



| <span data-ttu-id="7f089-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7f089-114">Requirement</span></span> | <span data-ttu-id="7f089-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7f089-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f089-116">Header</span><span class="sxs-lookup"><span data-stu-id="7f089-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7f089-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f089-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f089-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7f089-118">Library</span></span><br/> | <dl> <span data-ttu-id="7f089-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f089-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f089-120">См. также</span><span class="sxs-lookup"><span data-stu-id="7f089-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f089-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7f089-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7f089-122">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="7f089-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




