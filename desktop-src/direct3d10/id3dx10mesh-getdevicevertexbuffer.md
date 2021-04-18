---
description: 'Доступ к буферу вершин сетки после его фиксации на устройстве с помощью ID3DX10Mesh:: Коммиттодевице. Это отличается от ID3DX10Mesh:: Жетвертексбуффер, который возвращает буфер вершин до того, как он зафиксируется на устройстве.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'Метод ID3DX10Mesh:: Жетдевицевертексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713849"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="31de0-104">Метод ID3DX10Mesh:: Жетдевицевертексбуффер</span><span class="sxs-lookup"><span data-stu-id="31de0-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="31de0-105">Доступ к буферу вершин сетки после его фиксации на устройстве с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="31de0-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="31de0-106">Это отличается от [**ID3DX10Mesh:: жетвертексбуффер**](id3dx10mesh-getvertexbuffer.md), который возвращает буфер вершин до того, как он зафиксируется на устройстве.</span><span class="sxs-lookup"><span data-stu-id="31de0-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="31de0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31de0-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="31de0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="31de0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31de0-109">*iBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31de0-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31de0-110">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31de0-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31de0-111">Индекс, указывающий, к какому буферу вершин требуется доступ.</span><span class="sxs-lookup"><span data-stu-id="31de0-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="31de0-112">*ппвертексбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31de0-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31de0-113">Тип: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="31de0-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="31de0-114">Буфер вершин после его фиксации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="31de0-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31de0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31de0-115">Return value</span></span>

<span data-ttu-id="31de0-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31de0-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31de0-117">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="31de0-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31de0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="31de0-118">Requirements</span></span>



| <span data-ttu-id="31de0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="31de0-119">Requirement</span></span> | <span data-ttu-id="31de0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="31de0-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31de0-121">Header</span><span class="sxs-lookup"><span data-stu-id="31de0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31de0-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="31de0-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="31de0-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31de0-123">Library</span></span><br/> | <dl> <span data-ttu-id="31de0-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31de0-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31de0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31de0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31de0-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="31de0-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="31de0-127">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="31de0-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
