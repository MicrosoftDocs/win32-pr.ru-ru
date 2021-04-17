---
description: 'Доступ к буферу индекса сетки после его фиксации на устройстве с помощью ID3DX10Mesh:: Коммиттодевице. Это отличается от ID3DX10Mesh:: Жетиндексбуффер, который возвращает буфер индекса до того, как он зафиксируется на устройстве.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'Метод ID3DX10Mesh:: Жетдевицеиндексбуффер (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694234"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="05df5-104">Метод ID3DX10Mesh:: Жетдевицеиндексбуффер</span><span class="sxs-lookup"><span data-stu-id="05df5-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="05df5-105">Доступ к буферу индекса сетки после его фиксации на устройстве с помощью [**ID3DX10Mesh:: коммиттодевице**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="05df5-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="05df5-106">Это отличается от [**ID3DX10Mesh:: жетиндексбуффер**](id3dx10mesh-getindexbuffer.md), который возвращает буфер индекса до того, как он зафиксируется на устройстве.</span><span class="sxs-lookup"><span data-stu-id="05df5-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="05df5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05df5-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="05df5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05df5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05df5-109">*ппиндексбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="05df5-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05df5-110">Тип: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="05df5-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="05df5-111">Буфер индекса после его фиксации на устройстве.</span><span class="sxs-lookup"><span data-stu-id="05df5-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05df5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05df5-112">Return value</span></span>

<span data-ttu-id="05df5-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05df5-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05df5-114">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="05df5-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05df5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05df5-115">Remarks</span></span>

<span data-ttu-id="05df5-116">Если буфер индексов сетки еще не зафиксирован на устройстве, этот API будет автоматически зафиксировать буфер, прежде чем он вернет указатель на буфер.</span><span class="sxs-lookup"><span data-stu-id="05df5-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="05df5-117">Требования</span><span class="sxs-lookup"><span data-stu-id="05df5-117">Requirements</span></span>



| <span data-ttu-id="05df5-118">Требование</span><span class="sxs-lookup"><span data-stu-id="05df5-118">Requirement</span></span> | <span data-ttu-id="05df5-119">Значение</span><span class="sxs-lookup"><span data-stu-id="05df5-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05df5-120">Header</span><span class="sxs-lookup"><span data-stu-id="05df5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="05df5-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="05df5-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="05df5-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05df5-122">Library</span></span><br/> | <dl> <span data-ttu-id="05df5-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05df5-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05df5-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05df5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05df5-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="05df5-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="05df5-126">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="05df5-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




