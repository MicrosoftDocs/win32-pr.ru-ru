---
description: Загружает сетку из файла DirectX. x.
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: Функция D3DXLoadMeshFromX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354803"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="69117-103">Функция D3DXLoadMeshFromX</span><span class="sxs-lookup"><span data-stu-id="69117-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="69117-104">Загружает сетку из файла DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="69117-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="69117-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69117-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="69117-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="69117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69117-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69117-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69117-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69117-109">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="69117-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="69117-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="69117-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="69117-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="69117-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="69117-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="69117-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="69117-113">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69117-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69117-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69117-115">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , которое указывает параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="69117-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="69117-116">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69117-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-117">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="69117-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="69117-118">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="69117-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="69117-119">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69117-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-120">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="69117-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="69117-121">Указатель на буфер, содержащий соседических данных.</span><span class="sxs-lookup"><span data-stu-id="69117-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="69117-122">Смежные данные содержат массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="69117-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="69117-123">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="69117-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="69117-124">*ппматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69117-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="69117-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="69117-126">Указатель на буфер, содержащий данные о материалах.</span><span class="sxs-lookup"><span data-stu-id="69117-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="69117-127">Буфер содержит массив структур [**D3DXMATERIAL**](d3dxmaterial.md) , содержащий сведения из файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="69117-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="69117-128">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="69117-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="69117-129">*ппеффектинстанцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69117-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-130">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="69117-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="69117-131">Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке.</span><span class="sxs-lookup"><span data-stu-id="69117-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="69117-132">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="69117-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="69117-133">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="69117-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="69117-134">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="69117-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="69117-135">*пнумматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69117-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-136">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69117-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69117-137">Указатель на число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *ппматериалс* , когда метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="69117-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="69117-138">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="69117-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69117-139">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="69117-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="69117-140">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий загруженную сетку.</span><span class="sxs-lookup"><span data-stu-id="69117-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69117-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69117-141">Return value</span></span>

<span data-ttu-id="69117-142">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69117-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69117-143">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="69117-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69117-144">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="69117-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="69117-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69117-145">Remarks</span></span>

<span data-ttu-id="69117-146">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="69117-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="69117-147">Если определен Юникод, вызов функции разрешается в D3DXLoadMeshFromXW.</span><span class="sxs-lookup"><span data-stu-id="69117-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="69117-148">В противном случае вызов функции разрешается в D3DXLoadMeshFromXA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="69117-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="69117-149">Все сетки в файле будут свернуты в одну выходную сетку.</span><span class="sxs-lookup"><span data-stu-id="69117-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="69117-150">Если файл содержит иерархию рамок, все преобразования будут применены к сетке.</span><span class="sxs-lookup"><span data-stu-id="69117-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="69117-151">Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x.</span><span class="sxs-lookup"><span data-stu-id="69117-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="69117-152">Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="69117-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="69117-153">Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому.</span><span class="sxs-lookup"><span data-stu-id="69117-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="69117-154">Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя".</span><span class="sxs-lookup"><span data-stu-id="69117-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="69117-155">Он будет содержать строковое имя файла для текстуры.</span><span class="sxs-lookup"><span data-stu-id="69117-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="69117-156">Требования</span><span class="sxs-lookup"><span data-stu-id="69117-156">Requirements</span></span>



| <span data-ttu-id="69117-157">Требование</span><span class="sxs-lookup"><span data-stu-id="69117-157">Requirement</span></span> | <span data-ttu-id="69117-158">Значение</span><span class="sxs-lookup"><span data-stu-id="69117-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69117-159">Header</span><span class="sxs-lookup"><span data-stu-id="69117-159">Header</span></span><br/>  | <dl> <span data-ttu-id="69117-160"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="69117-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="69117-161">Библиотека</span><span class="sxs-lookup"><span data-stu-id="69117-161">Library</span></span><br/> | <dl> <span data-ttu-id="69117-162"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69117-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69117-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69117-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69117-164">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="69117-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="69117-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="69117-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="69117-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="69117-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
