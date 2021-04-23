---
description: Загружает сетку исправлений из объекта ID3DXFileData.
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: Функция D3DXLoadPatchMeshFromXof (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703745"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="0549f-103">Функция D3DXLoadPatchMeshFromXof</span><span class="sxs-lookup"><span data-stu-id="0549f-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="0549f-104">Загружает сетку исправлений из объекта [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="0549f-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0549f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0549f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="0549f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0549f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0549f-107">*пксофмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0549f-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-108">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="0549f-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="0549f-109">Указатель на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий файл данных файла для загрузки.</span><span class="sxs-lookup"><span data-stu-id="0549f-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="0549f-110">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0549f-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0549f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0549f-112">Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающее параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="0549f-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0549f-113">*pD3DDevice* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0549f-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-114">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0549f-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0549f-115">Указатель на устройство, из которого создается сетка.</span><span class="sxs-lookup"><span data-stu-id="0549f-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="0549f-116">*ппматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0549f-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-117">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0549f-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0549f-118">Массив материалов, содержащихся в сетке.</span><span class="sxs-lookup"><span data-stu-id="0549f-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="0549f-119">Каждый материал индексируется с помощью интерфейса [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0549f-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0549f-120">*ппеффектинстанцес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0549f-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-121">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0549f-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0549f-122">Указатель на буфер, содержащий массив экземпляров эффектов, по одному на группу атрибутов в возвращенной сетке.</span><span class="sxs-lookup"><span data-stu-id="0549f-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="0549f-123">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="0549f-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="0549f-124">См. [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="0549f-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="0549f-125">Дополнительные сведения о доступе к буферу см. в разделе [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0549f-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0549f-126">*пнумматериалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0549f-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-127">Тип: **пдворд**</span><span class="sxs-lookup"><span data-stu-id="0549f-127">Type: **PDWORD**</span></span>

<span data-ttu-id="0549f-128">Указатель, содержащий количество материалов в сетке.</span><span class="sxs-lookup"><span data-stu-id="0549f-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0549f-129">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0549f-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0549f-130">Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0549f-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="0549f-131">Адрес указателя на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий загруженную сетку.</span><span class="sxs-lookup"><span data-stu-id="0549f-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0549f-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0549f-132">Return value</span></span>

<span data-ttu-id="0549f-133">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0549f-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0549f-134">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0549f-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0549f-135">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0549f-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0549f-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0549f-136">Remarks</span></span>

<span data-ttu-id="0549f-137">Для файлов сетки, не содержащих сведений об экземпляре влияния, экземпляры эффектов по умолчанию будут сформированы на основе сведений о материалах в файле. x.</span><span class="sxs-lookup"><span data-stu-id="0549f-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="0549f-138">Экземпляр действия по умолчанию будет иметь значения по умолчанию, соответствующие элементам структуры [**D3DMATERIAL9**](d3dmaterial9.md) .</span><span class="sxs-lookup"><span data-stu-id="0549f-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="0549f-139">Имя текстуры по умолчанию также заполняется, но обрабатывается по-другому.</span><span class="sxs-lookup"><span data-stu-id="0549f-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="0549f-140">Имя будет иметь значение Texture0@Name , соответствующее переменной Effect с именем "Texture0" с заметкой "имя".</span><span class="sxs-lookup"><span data-stu-id="0549f-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="0549f-141">Он будет содержать строковое имя файла для текстуры.</span><span class="sxs-lookup"><span data-stu-id="0549f-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0549f-142">Требования</span><span class="sxs-lookup"><span data-stu-id="0549f-142">Requirements</span></span>



| <span data-ttu-id="0549f-143">Требование</span><span class="sxs-lookup"><span data-stu-id="0549f-143">Requirement</span></span> | <span data-ttu-id="0549f-144">Значение</span><span class="sxs-lookup"><span data-stu-id="0549f-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0549f-145">Header</span><span class="sxs-lookup"><span data-stu-id="0549f-145">Header</span></span><br/>  | <dl> <span data-ttu-id="0549f-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0549f-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0549f-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0549f-147">Library</span></span><br/> | <dl> <span data-ttu-id="0549f-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0549f-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0549f-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0549f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0549f-150">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="0549f-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="0549f-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="0549f-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="0549f-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="0549f-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
