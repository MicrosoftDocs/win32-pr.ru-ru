---
description: Загружает сетку из памяти.
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: Функция D3DXLoadMeshFromXInMemory (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703781"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="cb3a9-103">Функция D3DXLoadMeshFromXInMemory</span><span class="sxs-lookup"><span data-stu-id="cb3a9-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="cb3a9-104">Загружает сетку из памяти.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb3a9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="cb3a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb3a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3a9-107">*Память* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3a9-109">Указатель на буфер памяти, содержащий данные сетки.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-110">*Сизеофмемори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3a9-112">Размер файла в памяти, в байтах.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-113">*Параметры* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cb3a9-115">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , в котором указываются параметры создания сетки.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-116">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-117">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cb3a9-118">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-119">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-120">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3a9-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cb3a9-121">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3a9-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="cb3a9-122">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-123">*ппматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-124">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3a9-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cb3a9-125">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3a9-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="cb3a9-126">При возврате из этого метода этот параметр заполняется массивом структур [**D3DXMATERIAL**](d3dxmaterial.md) , содержащих сведения, сохраненные в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-127">*ппеффектинстанцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-128">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3a9-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cb3a9-129">Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="cb3a9-130">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="cb3a9-131">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="cb3a9-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="cb3a9-132">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="cb3a9-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-133">*пнумматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-134">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3a9-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb3a9-135">Указатель на число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *ппматериалс* , когда метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="cb3a9-136">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cb3a9-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3a9-137">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb3a9-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cb3a9-138">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий загруженную сетку.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3a9-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb3a9-139">Return value</span></span>

<span data-ttu-id="cb3a9-140">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cb3a9-141">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cb3a9-142">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb3a9-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb3a9-143">Remarks</span></span>

<span data-ttu-id="cb3a9-144">Все сетки в файле будут свернуты в одну выходную сетку.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="cb3a9-145">Если файл содержит иерархию рамок, все преобразования будут применены к сетке.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="cb3a9-146">Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="cb3a9-147">Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="cb3a9-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="cb3a9-148">Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="cb3a9-149">Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя".</span><span class="sxs-lookup"><span data-stu-id="cb3a9-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="cb3a9-150">Он будет содержать строковое имя файла для текстуры.</span><span class="sxs-lookup"><span data-stu-id="cb3a9-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3a9-151">Требования</span><span class="sxs-lookup"><span data-stu-id="cb3a9-151">Requirements</span></span>



| <span data-ttu-id="cb3a9-152">Требование</span><span class="sxs-lookup"><span data-stu-id="cb3a9-152">Requirement</span></span> | <span data-ttu-id="cb3a9-153">Значение</span><span class="sxs-lookup"><span data-stu-id="cb3a9-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3a9-154">Header</span><span class="sxs-lookup"><span data-stu-id="cb3a9-154">Header</span></span><br/>  | <dl> <span data-ttu-id="cb3a9-155"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb3a9-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cb3a9-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb3a9-156">Library</span></span><br/> | <dl> <span data-ttu-id="cb3a9-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb3a9-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb3a9-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb3a9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3a9-159">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="cb3a9-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="cb3a9-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="cb3a9-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="cb3a9-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
