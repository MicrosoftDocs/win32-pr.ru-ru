---
description: Зафиксируйте изменения, внесенные в сетку на устройстве, чтобы изменения можно было отобразить. Он должен вызываться после изменения данных сетки и до ее подготовки к просмотру. Сетка не может быть визуализирована, если она не зафиксирована на устройстве. См. примечания.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'Метод ID3DX10Mesh:: Коммиттодевице (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081872"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="95377-106">Метод ID3DX10Mesh:: Коммиттодевице</span><span class="sxs-lookup"><span data-stu-id="95377-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="95377-107">Зафиксируйте изменения, внесенные в сетку на устройстве, чтобы изменения можно было отобразить.</span><span class="sxs-lookup"><span data-stu-id="95377-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="95377-108">Он должен вызываться после изменения данных сетки и до ее подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="95377-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="95377-109">Сетка не может быть визуализирована, если она не зафиксирована на устройстве.</span><span class="sxs-lookup"><span data-stu-id="95377-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="95377-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="95377-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="95377-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95377-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="95377-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="95377-112">Parameters</span></span>

<span data-ttu-id="95377-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="95377-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="95377-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95377-114">Return value</span></span>

<span data-ttu-id="95377-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95377-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95377-116">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="95377-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95377-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95377-117">Remarks</span></span>

<span data-ttu-id="95377-118">При загрузке сетки данные загружаются в промежуточные ресурсы, что означает, что данные можно изменять, но не подготавливать к просмотру.</span><span class="sxs-lookup"><span data-stu-id="95377-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="95377-119">При вызове Коммиттодевице данные из промежуточных ресурсов копируются в ресурсы устройства, чтобы их можно было подготавливать к просмотру.</span><span class="sxs-lookup"><span data-stu-id="95377-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="95377-120">Несмотря на то, что данные фиксируются на устройстве, промежуточные ресурсы остаются и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="95377-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="95377-121">Если в промежуточные ресурсы вносятся какие либо изменения, промежуточные ресурсы должны быть зафиксированы на устройстве, чтобы эти изменения отображались на экране.</span><span class="sxs-lookup"><span data-stu-id="95377-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="95377-122">Требования</span><span class="sxs-lookup"><span data-stu-id="95377-122">Requirements</span></span>



| <span data-ttu-id="95377-123">Требование</span><span class="sxs-lookup"><span data-stu-id="95377-123">Requirement</span></span> | <span data-ttu-id="95377-124">Значение</span><span class="sxs-lookup"><span data-stu-id="95377-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95377-125">Header</span><span class="sxs-lookup"><span data-stu-id="95377-125">Header</span></span><br/>  | <dl> <span data-ttu-id="95377-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="95377-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="95377-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95377-127">Library</span></span><br/> | <dl> <span data-ttu-id="95377-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95377-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95377-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95377-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95377-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="95377-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="95377-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="95377-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




