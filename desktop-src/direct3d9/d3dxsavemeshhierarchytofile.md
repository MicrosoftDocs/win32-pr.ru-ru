---
description: Создает файл. x и сохраняет иерархию сетки и соответствующие анимации в ней.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: Функция D3DXSaveMeshHierarchyToFile (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694136"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="36177-103">Функция D3DXSaveMeshHierarchyToFile</span><span class="sxs-lookup"><span data-stu-id="36177-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="36177-104">Создает файл. x и сохраняет иерархию сетки и соответствующие анимации в ней.</span><span class="sxs-lookup"><span data-stu-id="36177-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="36177-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36177-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="36177-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36177-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36177-107">*пфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36177-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36177-108">Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36177-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36177-109">Указатель на строку, указывающую имя файла x, определяющего сохраненную сетку.</span><span class="sxs-lookup"><span data-stu-id="36177-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="36177-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="36177-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="36177-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="36177-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="36177-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="36177-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="36177-113">*Ксформат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36177-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36177-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36177-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36177-115">Формат файла. x (Text или binary, сжатый или не).</span><span class="sxs-lookup"><span data-stu-id="36177-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="36177-116">См. раздел D3DXF \_ FILEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="36177-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="36177-117">\_Сжатый D3DXF FILEFORMAT \_ можно объединить (с помощью логического или) с \_ \_ флагами текста D3DXF FILEFORMAT binary или D3DXF \_ FILEFORMAT, \_ чтобы уменьшить размер выходного файла.</span><span class="sxs-lookup"><span data-stu-id="36177-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="36177-118">*пфрамерут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36177-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36177-119">Тип: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="36177-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="36177-120">Корневой узел для сохраняемой иерархии.</span><span class="sxs-lookup"><span data-stu-id="36177-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="36177-121">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="36177-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="36177-122">*панимконтроллер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36177-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36177-123">Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="36177-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="36177-124">Контроллер анимации, на котором хранятся наборы анимации.</span><span class="sxs-lookup"><span data-stu-id="36177-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="36177-125">См. [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="36177-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="36177-126">*пусердатасавер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36177-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36177-127">Тип: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="36177-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="36177-128">Предоставляемый приложением интерфейс, позволяющий сохранять данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="36177-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="36177-129">См. [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span><span class="sxs-lookup"><span data-stu-id="36177-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36177-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36177-130">Return value</span></span>

<span data-ttu-id="36177-131">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36177-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36177-132">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="36177-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="36177-133">Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="36177-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="36177-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36177-134">Remarks</span></span>

<span data-ttu-id="36177-135">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="36177-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="36177-136">Если определен Юникод, вызов функции разрешается в D3DXSaveMeshHierarchyToFileW.</span><span class="sxs-lookup"><span data-stu-id="36177-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="36177-137">В противном случае вызов функции разрешается в D3DXSaveMeshHierarchyToFileA.</span><span class="sxs-lookup"><span data-stu-id="36177-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="36177-138">Эта функция не сохраняет сжатые наборы анимации.</span><span class="sxs-lookup"><span data-stu-id="36177-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="36177-139">Требования</span><span class="sxs-lookup"><span data-stu-id="36177-139">Requirements</span></span>



| <span data-ttu-id="36177-140">Требование</span><span class="sxs-lookup"><span data-stu-id="36177-140">Requirement</span></span> | <span data-ttu-id="36177-141">Значение</span><span class="sxs-lookup"><span data-stu-id="36177-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36177-142">Header</span><span class="sxs-lookup"><span data-stu-id="36177-142">Header</span></span><br/>  | <dl> <span data-ttu-id="36177-143"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="36177-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="36177-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="36177-144">Library</span></span><br/> | <dl> <span data-ttu-id="36177-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36177-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36177-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36177-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36177-147">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="36177-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="36177-148">Ссылка на X файл</span><span class="sxs-lookup"><span data-stu-id="36177-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
