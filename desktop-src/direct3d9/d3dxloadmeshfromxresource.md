---
description: Загружает сетку из ресурса.
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: Функция D3DXLoadMeshFromXResource (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821061"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="7aa03-103">Функция D3DXLoadMeshFromXResource</span><span class="sxs-lookup"><span data-stu-id="7aa03-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="7aa03-104">Загружает сетку из ресурса.</span><span class="sxs-lookup"><span data-stu-id="7aa03-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa03-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7aa03-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="7aa03-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7aa03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7aa03-107">*Модуль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-108">Тип: **[ **хмодуле**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7aa03-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7aa03-109">Указатель на модуль, в котором находится ресурс, или **значение NULL** для модуля, связанного с образом, операционной системой, используемой для создания текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="7aa03-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="7aa03-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="7aa03-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-111">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-112">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7aa03-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7aa03-113">Указатель на строку, указывающую ресурс, из которого нужно создать сетку.</span><span class="sxs-lookup"><span data-stu-id="7aa03-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="7aa03-114">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="7aa03-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-115">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-116">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7aa03-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7aa03-117">Указатель на строку, указывающую тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7aa03-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="7aa03-118">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="7aa03-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-119">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-120">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7aa03-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7aa03-121">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , задающих параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="7aa03-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-122">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-123">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7aa03-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7aa03-124">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="7aa03-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-125">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-126">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7aa03-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7aa03-127">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa03-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="7aa03-128">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="7aa03-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-129">*ппматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-130">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7aa03-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7aa03-131">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa03-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="7aa03-132">При возврате из этого метода этот параметр заполняется массивом структур [**D3DXMATERIAL**](d3dxmaterial.md) , содержащих сведения, сохраненные в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="7aa03-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-133">*ппеффектинстанцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-134">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7aa03-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7aa03-135">Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке.</span><span class="sxs-lookup"><span data-stu-id="7aa03-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="7aa03-136">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="7aa03-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="7aa03-137">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="7aa03-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="7aa03-138">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7aa03-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-139">*пнумматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-140">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7aa03-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7aa03-141">Указатель на число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *ппматериалс* , когда метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7aa03-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="7aa03-142">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7aa03-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7aa03-143">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7aa03-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="7aa03-144">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий загруженную сетку.</span><span class="sxs-lookup"><span data-stu-id="7aa03-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7aa03-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7aa03-145">Return value</span></span>

<span data-ttu-id="7aa03-146">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7aa03-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7aa03-147">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7aa03-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7aa03-148">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7aa03-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aa03-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7aa03-149">Remarks</span></span>

<span data-ttu-id="7aa03-150">Дополнительные сведения о модулях, именах и параметрах типов см. в разделе [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) .</span><span class="sxs-lookup"><span data-stu-id="7aa03-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="7aa03-151">Все сетки в файле будут свернуты в одну выходную сетку.</span><span class="sxs-lookup"><span data-stu-id="7aa03-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="7aa03-152">Если файл содержит иерархию рамок, все преобразования будут применены к сетке.</span><span class="sxs-lookup"><span data-stu-id="7aa03-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="7aa03-153">Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x.</span><span class="sxs-lookup"><span data-stu-id="7aa03-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="7aa03-154">Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="7aa03-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="7aa03-155">Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому.</span><span class="sxs-lookup"><span data-stu-id="7aa03-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="7aa03-156">Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя".</span><span class="sxs-lookup"><span data-stu-id="7aa03-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="7aa03-157">Он будет содержать строковое имя файла для текстуры.</span><span class="sxs-lookup"><span data-stu-id="7aa03-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa03-158">Требования</span><span class="sxs-lookup"><span data-stu-id="7aa03-158">Requirements</span></span>



| <span data-ttu-id="7aa03-159">Требование</span><span class="sxs-lookup"><span data-stu-id="7aa03-159">Requirement</span></span> | <span data-ttu-id="7aa03-160">Значение</span><span class="sxs-lookup"><span data-stu-id="7aa03-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa03-161">Header</span><span class="sxs-lookup"><span data-stu-id="7aa03-161">Header</span></span><br/>  | <dl> <span data-ttu-id="7aa03-162"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7aa03-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7aa03-163">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7aa03-163">Library</span></span><br/> | <dl> <span data-ttu-id="7aa03-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7aa03-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7aa03-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7aa03-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa03-166">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="7aa03-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="7aa03-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7aa03-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="7aa03-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="7aa03-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
