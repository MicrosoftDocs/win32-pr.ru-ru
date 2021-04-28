---
description: Функция D3DXSHPRTCompSplitMeshSC — используется со сжатыми результатами эмулятора предварительно вычисленной радианценой пересылки (PRT).
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: Функция D3DXSHPRTCompSplitMeshSC (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093902"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="84fd1-103">Функция D3DXSHPRTCompSplitMeshSC</span><span class="sxs-lookup"><span data-stu-id="84fd1-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="84fd1-104">Используется с сжатыми результатами симулятора предварительно вычисленной радианценой пересылки (PRT).</span><span class="sxs-lookup"><span data-stu-id="84fd1-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="84fd1-105">После вызова [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) эту функцию можно использовать для разделения сетки на группу лиц или вершин на супер-кластер.</span><span class="sxs-lookup"><span data-stu-id="84fd1-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="84fd1-106">Каждый супер кластер содержит все грани, которые содержат любую вершину, классифицированную в одном из его кластеров.</span><span class="sxs-lookup"><span data-stu-id="84fd1-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="84fd1-107">Все вершины, подключенные к этому набору лиц, также включаются в возвращаемый массив Ппвертстатус, который указывает, принадлежит ли вершина к Super кластеру.</span><span class="sxs-lookup"><span data-stu-id="84fd1-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fd1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84fd1-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="84fd1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="84fd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84fd1-110">*пклустеридс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84fd1-112">Идентификаторы кластера *нумвертицес* (извлеченные из сжатого буфера).</span><span class="sxs-lookup"><span data-stu-id="84fd1-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-113">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-115">Количество вершин в исходной сетке.</span><span class="sxs-lookup"><span data-stu-id="84fd1-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-116">*Нумкс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-118">Количество кластеров (входной параметр для сжатия).</span><span class="sxs-lookup"><span data-stu-id="84fd1-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-119">*псклустеридс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-120">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84fd1-121">Массив размера *нумкс* , который будет содержать идентификаторы Super Cluster.</span><span class="sxs-lookup"><span data-stu-id="84fd1-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-122">*Нумскс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-124">Количество супер кластеров, выделенных в [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span><span class="sxs-lookup"><span data-stu-id="84fd1-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-125">*пинпутиб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-126">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-127">Буфер необработанных индексов для сетки.</span><span class="sxs-lookup"><span data-stu-id="84fd1-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="84fd1-128">Формат зависит от *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="84fd1-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-129">*InputIBIs32Bit* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-130">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-131">Если **значение — true**, буфер индекса имеет значение 32 бит; в противном случае — 16 бит.</span><span class="sxs-lookup"><span data-stu-id="84fd1-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-132">*Нумфацес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-133">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-134">Число граней в исходной сети (*пинпутиб* в три раза больше этой длины).</span><span class="sxs-lookup"><span data-stu-id="84fd1-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-135">*ппибдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-136">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="84fd1-137">Буфер необработанных индексов, который будет содержать полученные разделенные фрагменты.</span><span class="sxs-lookup"><span data-stu-id="84fd1-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="84fd1-138">Формат, определенный параметром *InputIBIs32Bit*.</span><span class="sxs-lookup"><span data-stu-id="84fd1-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="84fd1-139">Выделено функцией.</span><span class="sxs-lookup"><span data-stu-id="84fd1-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-140">*пибдаталенгс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-141">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84fd1-142">Длина *ппибдата*, назначенная в функции.</span><span class="sxs-lookup"><span data-stu-id="84fd1-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-143">*OutputIBIs32Bit* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-144">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84fd1-145">Если **значение — true**, выделяет массив целых чисел без знака; в противном случае выделяет короткий массив без знака.</span><span class="sxs-lookup"><span data-stu-id="84fd1-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-146">*ппфацеремап* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-147">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="84fd1-148">Сопоставление каждого лица в *ппибдата* с исходными лицами.</span><span class="sxs-lookup"><span data-stu-id="84fd1-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="84fd1-149">Длина — \* *пибдаталенгс*/3.</span><span class="sxs-lookup"><span data-stu-id="84fd1-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-150">*ппвертдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-151">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="84fd1-152">Новая структура данных вершин.</span><span class="sxs-lookup"><span data-stu-id="84fd1-152">New vertex data structure.</span></span> <span data-ttu-id="84fd1-153">Размер *пвертдаталенгс*.</span><span class="sxs-lookup"><span data-stu-id="84fd1-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-154">*пвертдаталенгс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-155">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84fd1-156">Количество новых вершин в разделенной сетке.</span><span class="sxs-lookup"><span data-stu-id="84fd1-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="84fd1-157">Назначено в функции.</span><span class="sxs-lookup"><span data-stu-id="84fd1-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-158">*пскклустерлист* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-159">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84fd1-160">Массив длины, *нумкс* , что *пскдата* индексы в (поля *пклустеридс* \* ) для каждого кластера, содержит кластеры, упорядоченные по подкластерам.</span><span class="sxs-lookup"><span data-stu-id="84fd1-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="84fd1-161">*пскдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="84fd1-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84fd1-162">Тип: **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="84fd1-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="84fd1-163">Структура на супер кластер.</span><span class="sxs-lookup"><span data-stu-id="84fd1-163">Structure per super cluster.</span></span> <span data-ttu-id="84fd1-164">Содержит индексы в *ппибдата*, *пскклустерлист* и *ппвертдата*.</span><span class="sxs-lookup"><span data-stu-id="84fd1-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84fd1-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84fd1-165">Return value</span></span>

<span data-ttu-id="84fd1-166">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="84fd1-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="84fd1-167">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="84fd1-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="84fd1-168">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="84fd1-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fd1-169">Требования</span><span class="sxs-lookup"><span data-stu-id="84fd1-169">Requirements</span></span>



| <span data-ttu-id="84fd1-170">Требование</span><span class="sxs-lookup"><span data-stu-id="84fd1-170">Requirement</span></span> | <span data-ttu-id="84fd1-171">Значение</span><span class="sxs-lookup"><span data-stu-id="84fd1-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84fd1-172">Header</span><span class="sxs-lookup"><span data-stu-id="84fd1-172">Header</span></span><br/>  | <dl> <span data-ttu-id="84fd1-173"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="84fd1-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="84fd1-174">Библиотека</span><span class="sxs-lookup"><span data-stu-id="84fd1-174">Library</span></span><br/> | <dl> <span data-ttu-id="84fd1-175"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84fd1-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84fd1-176">См. также</span><span class="sxs-lookup"><span data-stu-id="84fd1-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fd1-177">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="84fd1-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
