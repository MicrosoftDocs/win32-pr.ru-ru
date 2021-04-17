---
description: Нарисуйте несколько экземпляров одного подмножества сетки.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: 'ID3DX10Mesh: метод:D Равсубсетинстанцед (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674740"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="94ace-103">ID3DX10Mesh: метод:D Равсубсетинстанцед</span><span class="sxs-lookup"><span data-stu-id="94ace-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="94ace-104">Нарисуйте несколько экземпляров одного подмножества сетки.</span><span class="sxs-lookup"><span data-stu-id="94ace-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ace-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94ace-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="94ace-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94ace-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ace-107">*Аттрибид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ace-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ace-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94ace-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="94ace-109">Указывает подмножество рисуемой сетки.</span><span class="sxs-lookup"><span data-stu-id="94ace-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="94ace-110">Это значение используется для различения лиц в сетке как принадлежащих одной или нескольким группам атрибутов.</span><span class="sxs-lookup"><span data-stu-id="94ace-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="94ace-111">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="94ace-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="94ace-112">*InstanceCount* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ace-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ace-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94ace-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="94ace-114">Число экземпляров для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="94ace-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="94ace-115">*Стартинстанцелокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ace-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ace-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="94ace-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="94ace-117">Экземпляр, с которого начинается выборка из каждого буфера, помеченного как данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="94ace-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ace-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94ace-118">Return value</span></span>

<span data-ttu-id="94ace-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="94ace-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="94ace-120">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="94ace-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="94ace-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94ace-121">Remarks</span></span>

<span data-ttu-id="94ace-122">Сетка содержит таблицу атрибутов.</span><span class="sxs-lookup"><span data-stu-id="94ace-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="94ace-123">Таблица атрибутов может разделить сетку на подмножества, где каждое подмножество определяется с помощью идентификатора атрибута.</span><span class="sxs-lookup"><span data-stu-id="94ace-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="94ace-124">Например, сетка с 200 лицами, разделенная на три подмножества, может иметь таблицу атрибутов, которая выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="94ace-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



|            |                 |
|------------|-----------------|
| <span data-ttu-id="94ace-125">Аттрибид 0</span><span class="sxs-lookup"><span data-stu-id="94ace-125">AttribID 0</span></span> | <span data-ttu-id="94ace-126">Лица 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="94ace-126">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="94ace-127">Аттрибид 1</span><span class="sxs-lookup"><span data-stu-id="94ace-127">AttribID 1</span></span> | <span data-ttu-id="94ace-128">Лица 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="94ace-128">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="94ace-129">Аттрибид 2</span><span class="sxs-lookup"><span data-stu-id="94ace-129">AttribID 2</span></span> | <span data-ttu-id="94ace-130">Лица 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="94ace-130">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="94ace-131">Создание экземпляров может увеличить производительность, повторно используя ту же геометрию для рисования нескольких объектов в сцене.</span><span class="sxs-lookup"><span data-stu-id="94ace-131">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="94ace-132">Одним из примеров создания экземпляров может быть Рисование одного и того же объекта с разными позициями и цветами.</span><span class="sxs-lookup"><span data-stu-id="94ace-132">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="94ace-133">Для индексирования требуется несколько буферов вершин: по крайней мере один для данных на вершину и второй буфер для данных каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="94ace-133">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="94ace-134">Отрисовка экземпляров с помощью Дравсубсетинстанцед очень похожа на процесс, используемый с [**ID3D10Device::D равиндексединстанцед**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) , который описан в [примере](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)с созданием экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94ace-134">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="94ace-135">Ключевое различие при использовании Дравсубсетинстанцед заключается в том, что буферы вершин и индексы должны быть извлечены из объекта [**интерфейса ID3DX10Mesh**](id3dx10mesh.md) , прежде чем можно будет объединить данные о создании экземпляров.</span><span class="sxs-lookup"><span data-stu-id="94ace-135">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="94ace-136">Следующий код иллюстрирует извлечение буферов вершин и индексов из объекта сетки.</span><span class="sxs-lookup"><span data-stu-id="94ace-136">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="94ace-137">Требования</span><span class="sxs-lookup"><span data-stu-id="94ace-137">Requirements</span></span>



| <span data-ttu-id="94ace-138">Требование</span><span class="sxs-lookup"><span data-stu-id="94ace-138">Requirement</span></span> | <span data-ttu-id="94ace-139">Значение</span><span class="sxs-lookup"><span data-stu-id="94ace-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94ace-140">Header</span><span class="sxs-lookup"><span data-stu-id="94ace-140">Header</span></span><br/>  | <dl> <span data-ttu-id="94ace-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="94ace-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="94ace-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94ace-142">Library</span></span><br/> | <dl> <span data-ttu-id="94ace-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94ace-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94ace-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94ace-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ace-145">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="94ace-145">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="94ace-146">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="94ace-146">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
