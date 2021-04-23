---
description: Сохраняет сетку в файл. x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: Функция D3DXSaveMeshToX (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694135"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="38e91-103">Функция D3DXSaveMeshToX</span><span class="sxs-lookup"><span data-stu-id="38e91-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="38e91-104">Сохраняет сетку в файл. x.</span><span class="sxs-lookup"><span data-stu-id="38e91-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38e91-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="38e91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="38e91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e91-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38e91-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38e91-109">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="38e91-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="38e91-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="38e91-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="38e91-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="38e91-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="38e91-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="38e91-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="38e91-113">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-114">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="38e91-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="38e91-115">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий сетку для сохранения в файл. x.</span><span class="sxs-lookup"><span data-stu-id="38e91-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="38e91-116">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-117">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="38e91-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38e91-118">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="38e91-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="38e91-119">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="38e91-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38e91-120">*пматериалс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-121">Тип: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="38e91-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="38e91-122">Указатель на массив структур [**D3DXMATERIAL**](d3dxmaterial.md) , содержащий сведения о материалах, которые должны быть сохранены в файле. x.</span><span class="sxs-lookup"><span data-stu-id="38e91-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="38e91-123">*пеффектинстанцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-124">Тип: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="38e91-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="38e91-125">Указатель на массив экземпляров эффектов, по одному на группу атрибутов в сетке.</span><span class="sxs-lookup"><span data-stu-id="38e91-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="38e91-126">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="38e91-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="38e91-127">Экземпляр Effect — это конкретный экземпляр сведений о состоянии, используемый для инициализации результата.</span><span class="sxs-lookup"><span data-stu-id="38e91-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="38e91-128">Дополнительные сведения см. в разделе [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="38e91-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="38e91-129">*Нумматериалс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-130">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38e91-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38e91-131">Число структур [**D3DXMATERIAL**](d3dxmaterial.md) в массиве *пматериалс* .</span><span class="sxs-lookup"><span data-stu-id="38e91-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="38e91-132">*Формат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="38e91-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e91-133">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38e91-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38e91-134">Сочетание формата файла и параметров сохранения при сохранении файла. x.</span><span class="sxs-lookup"><span data-stu-id="38e91-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="38e91-135">См. раздел [константы файла D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md).</span><span class="sxs-lookup"><span data-stu-id="38e91-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e91-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38e91-136">Return value</span></span>

<span data-ttu-id="38e91-137">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38e91-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38e91-138">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="38e91-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38e91-139">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="38e91-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e91-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38e91-140">Remarks</span></span>

<span data-ttu-id="38e91-141">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="38e91-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="38e91-142">Если определен Юникод, вызов функции разрешается в D3DXSaveMeshToXW.</span><span class="sxs-lookup"><span data-stu-id="38e91-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="38e91-143">В противном случае вызов функции разрешается в D3DXSaveMeshToXA, так как используются строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="38e91-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="38e91-144">Формат файла по умолчанию — binary; Однако если файл указан как как двоичный, так и текстовый файл, он будет сохранен как текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="38e91-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="38e91-145">Независимо от формата файла, можно также использовать сжатый формат для уменьшения размера файла.</span><span class="sxs-lookup"><span data-stu-id="38e91-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="38e91-146">Ниже приведен типичный пример кода использования этой функции.</span><span class="sxs-lookup"><span data-stu-id="38e91-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="38e91-147">Требования</span><span class="sxs-lookup"><span data-stu-id="38e91-147">Requirements</span></span>



| <span data-ttu-id="38e91-148">Требование</span><span class="sxs-lookup"><span data-stu-id="38e91-148">Requirement</span></span> | <span data-ttu-id="38e91-149">Значение</span><span class="sxs-lookup"><span data-stu-id="38e91-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38e91-150">Header</span><span class="sxs-lookup"><span data-stu-id="38e91-150">Header</span></span><br/>  | <dl> <span data-ttu-id="38e91-151"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="38e91-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="38e91-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="38e91-152">Library</span></span><br/> | <dl> <span data-ttu-id="38e91-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38e91-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38e91-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38e91-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e91-155">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="38e91-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="38e91-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="38e91-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="38e91-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="38e91-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
