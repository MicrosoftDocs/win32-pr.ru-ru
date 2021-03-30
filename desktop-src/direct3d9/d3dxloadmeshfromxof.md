---
description: Загружает сетку из объекта ID3DXFileData.
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: Функция D3DXLoadMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354800"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="9f2d9-103">Функция D3DXLoadMeshFromXof</span><span class="sxs-lookup"><span data-stu-id="9f2d9-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="9f2d9-104">Загружает сетку из объекта [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="9f2d9-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f2d9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9f2d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f2d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2d9-107">*пксофмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-108">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="9f2d9-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="9f2d9-109">Указатель на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий файл данных файла для загрузки.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-110">*Параметры* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f2d9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f2d9-112">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , в котором указываются параметры создания сетки.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-114">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9f2d9-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9f2d9-115">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-116">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-117">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f2d9-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9f2d9-118">Указатель на буфер, содержащий соседических данных.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="9f2d9-119">Смежные данные содержат массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="9f2d9-120">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9f2d9-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-121">*ппматериалс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-122">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f2d9-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9f2d9-123">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9f2d9-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="9f2d9-124">Когда метод возвращает значение, этот параметр заполняется массивом структур [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="9f2d9-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-125">*ппеффектинстанцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-126">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f2d9-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9f2d9-127">Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="9f2d9-128">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="9f2d9-129">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="9f2d9-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="9f2d9-130">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9f2d9-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-131">*пнумматериалс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-132">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f2d9-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f2d9-133">Указатель на число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *ппматериалс* , когда метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="9f2d9-134">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9f2d9-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2d9-135">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f2d9-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9f2d9-136">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий загруженную сетку.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2d9-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f2d9-137">Return value</span></span>

<span data-ttu-id="9f2d9-138">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f2d9-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f2d9-139">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f2d9-140">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f2d9-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f2d9-141">Remarks</span></span>

<span data-ttu-id="9f2d9-142">Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="9f2d9-143">Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="9f2d9-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="9f2d9-144">Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="9f2d9-145">Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя".</span><span class="sxs-lookup"><span data-stu-id="9f2d9-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="9f2d9-146">Он будет содержать строковое имя файла для текстуры.</span><span class="sxs-lookup"><span data-stu-id="9f2d9-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2d9-147">Требования</span><span class="sxs-lookup"><span data-stu-id="9f2d9-147">Requirements</span></span>



| <span data-ttu-id="9f2d9-148">Требование</span><span class="sxs-lookup"><span data-stu-id="9f2d9-148">Requirement</span></span> | <span data-ttu-id="9f2d9-149">Значение</span><span class="sxs-lookup"><span data-stu-id="9f2d9-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2d9-150">Header</span><span class="sxs-lookup"><span data-stu-id="9f2d9-150">Header</span></span><br/>  | <dl> <span data-ttu-id="9f2d9-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f2d9-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9f2d9-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f2d9-152">Library</span></span><br/> | <dl> <span data-ttu-id="9f2d9-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f2d9-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f2d9-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f2d9-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2d9-155">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="9f2d9-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="9f2d9-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9f2d9-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="9f2d9-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="9f2d9-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
