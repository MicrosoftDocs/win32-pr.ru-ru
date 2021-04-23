---
description: Загружает сетку обложки из объекта данных файла DirectX. x.
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: Функция D3DXLoadSkinMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820956"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="d7886-103">Функция D3DXLoadSkinMeshFromXof</span><span class="sxs-lookup"><span data-stu-id="d7886-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="d7886-104">Загружает сетку обложки из объекта данных файла DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="d7886-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7886-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7886-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d7886-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7886-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7886-107">*пксофмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7886-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-108">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="d7886-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="d7886-109">Указатель на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий файл данных файла для загрузки.</span><span class="sxs-lookup"><span data-stu-id="d7886-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-110">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7886-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d7886-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d7886-112">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , в котором указываются параметры создания сетки.</span><span class="sxs-lookup"><span data-stu-id="d7886-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-113">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7886-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-114">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d7886-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d7886-115">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="d7886-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-116">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7886-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-117">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7886-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d7886-118">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d7886-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="d7886-119">При возврате из этого метода этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="d7886-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-120">*ппматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7886-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-121">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7886-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d7886-122">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="d7886-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="d7886-123">Когда метод возвращает значение, этот параметр заполняется массивом структур [**D3DXMATERIAL**](d3dxmaterial.md) .</span><span class="sxs-lookup"><span data-stu-id="d7886-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-124">*ппеффектинстанцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7886-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7886-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d7886-126">Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке.</span><span class="sxs-lookup"><span data-stu-id="d7886-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="d7886-127">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="d7886-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="d7886-128">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="d7886-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="d7886-129">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="d7886-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7886-130">*пматаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7886-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-131">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7886-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d7886-132">Указатель на число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *ппматериалс* , когда метод возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d7886-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-133">*ппскининфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7886-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-134">Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7886-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="d7886-135">Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий сведения о обложках.</span><span class="sxs-lookup"><span data-stu-id="d7886-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="d7886-136">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7886-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7886-137">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7886-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d7886-138">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , который представляет загруженную сетку.</span><span class="sxs-lookup"><span data-stu-id="d7886-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7886-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7886-139">Return value</span></span>

<span data-ttu-id="d7886-140">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d7886-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d7886-141">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d7886-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d7886-142">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d7886-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="d7886-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7886-143">Remarks</span></span>

<span data-ttu-id="d7886-144">Этот метод принимает указатель на внутренний объект в файле x, позволяя загрузить иерархию рамок.</span><span class="sxs-lookup"><span data-stu-id="d7886-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="d7886-145">Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x.</span><span class="sxs-lookup"><span data-stu-id="d7886-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="d7886-146">Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="d7886-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="d7886-147">Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому.</span><span class="sxs-lookup"><span data-stu-id="d7886-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="d7886-148">Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя".</span><span class="sxs-lookup"><span data-stu-id="d7886-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="d7886-149">Он будет содержать строковое имя файла для текстуры.</span><span class="sxs-lookup"><span data-stu-id="d7886-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7886-150">Требования</span><span class="sxs-lookup"><span data-stu-id="d7886-150">Requirements</span></span>



| <span data-ttu-id="d7886-151">Требование</span><span class="sxs-lookup"><span data-stu-id="d7886-151">Requirement</span></span> | <span data-ttu-id="d7886-152">Значение</span><span class="sxs-lookup"><span data-stu-id="d7886-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7886-153">Header</span><span class="sxs-lookup"><span data-stu-id="d7886-153">Header</span></span><br/>  | <dl> <span data-ttu-id="d7886-154"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7886-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d7886-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d7886-155">Library</span></span><br/> | <dl> <span data-ttu-id="d7886-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7886-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7886-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7886-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7886-158">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="d7886-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d7886-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d7886-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="d7886-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="d7886-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
