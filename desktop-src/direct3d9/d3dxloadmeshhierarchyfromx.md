---
description: Функция D3DXLoadMeshHierarchyFromX — загружает первую иерархию кадров из файла. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: Функция D3DXLoadMeshHierarchyFromX (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b6f6f08e10155509df800cca3cb3788d6b27e520
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114362"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="5c6e7-103">Функция D3DXLoadMeshHierarchyFromX</span><span class="sxs-lookup"><span data-stu-id="5c6e7-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="5c6e7-104">Загружает первую иерархию кадров из файла. x.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c6e7-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="5c6e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c6e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c6e7-107">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-108">Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c6e7-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c6e7-109">Указатель на строку, указывающую имя файла.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="5c6e7-110">Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5c6e7-111">В противном случае строковый тип данных разрешается в LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5c6e7-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e7-113">*Мешоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c6e7-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c6e7-115">Сочетание одного или нескольких флагов из перечисления [**D3DXMESH**](./d3dxmesh.md) , задающих параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e7-116">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-117">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5c6e7-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5c6e7-118">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e7-119">*паллок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-120">Тип: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="5c6e7-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="5c6e7-121">Указатель на интерфейс [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6e7-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e7-122">*пусердаталоадер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-123">Тип: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="5c6e7-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="5c6e7-124">Предоставленный приложением интерфейс, позволяющий загружать пользовательские данные.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="5c6e7-125">См. [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e7-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c6e7-126">*ппфрамехиерарчи* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-127">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c6e7-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="5c6e7-128">Возвращает указатель на иерархию загруженных кадров.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="5c6e7-129">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e7-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c6e7-130">*ппанимконтроллер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5c6e7-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c6e7-131">Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="5c6e7-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="5c6e7-132">Возвращает указатель на контроллер анимации, соответствующий анимации в файле. x.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="5c6e7-133">Он создается с отслеживанием и событиями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-133">This is created with default tracks and events.</span></span> <span data-ttu-id="5c6e7-134">См. [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e7-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c6e7-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c6e7-135">Return value</span></span>

<span data-ttu-id="5c6e7-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c6e7-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c6e7-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5c6e7-138">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c6e7-139">Remarks</span><span class="sxs-lookup"><span data-stu-id="5c6e7-139">Remarks</span></span>

<span data-ttu-id="5c6e7-140">Параметр компилятора также определяет версию функции.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5c6e7-141">Если определен Юникод, вызов функции разрешается в D3DXLoadMeshHierarchyFromXW.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="5c6e7-142">В противном случае вызов функции разрешается в D3DXLoadMeshHierarchyFromXA.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="5c6e7-143">Все сетки в файле будут свернуты в одну выходную сетку.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="5c6e7-144">Если файл содержит иерархию рамок, все преобразования будут применены к сетке.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="5c6e7-145">**D3DXLoadMeshHierarchyFromX** загружает данные анимации и иерархию кадров из файла. x.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="5c6e7-146">Он сканирует файл x и строит иерархию кадров и контроллер анимации в соответствии с объектом, производным от [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), который передается в него через паллок.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="5c6e7-147">Для загрузки данных необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="5c6e7-148">Производные [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), реализующие каждый метод.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="5c6e7-149">Это определяет, как выделяются и освобождаются фреймы и сетки.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="5c6e7-150">Производные [**ID3DXLoadUserData**](id3dxloaduserdata.md), реализующие каждый метод.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="5c6e7-151">Если файл. x не содержит внедренных пользовательских данных или его не требуется, можно пропустить эту часть.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="5c6e7-152">Создайте объект класса [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) и, при необходимости, класс лоадусердата.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="5c6e7-153">Нет необходимости самостоятельно вызывать методы этих объектов.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="5c6e7-154">Вызовите **D3DXLoadMeshHierarchyFromX**, передав объект [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) и объект [**ID3DXLoadUserData**](id3dxloaduserdata.md) (или **значение NULL**), чтобы создать иерархию кадров и контроллер анимации.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="5c6e7-155">Все наборы и кадры анимации автоматически регистрируются в контроллере анимации.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="5c6e7-156">Во время загрузки [**креатефраме**](id3dxallocatehierarchy--createframe.md) и [**лоадфрамечилддата**](id3dxloaduserdata--loadframechilddata.md) вызываются обратно в каждом кадре для управления загрузкой и выделением кадра.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="5c6e7-157">Приложение определяет эти методы для управления сохранением кадров.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="5c6e7-158">[**Креатемешконтаинер**](id3dxallocatehierarchy--createmeshcontainer.md) и [**лоадмешчилддата**](id3dxloaduserdata--loadmeshchilddata.md) вызываются обратно для каждого объекта сетки, чтобы управлять загрузкой и выделением объектов сетки.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="5c6e7-159">[**Лоадтоплевелдата**](id3dxloaduserdata--loadtopleveldata.md) вызывается обратно для каждого объекта верхнего уровня, который не загружается другими методами.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="5c6e7-160">Чтобы освободить эти данные, вызовите ID3DXAnimationController:: Release, чтобы освободить наборы анимации, и [**D3DXFRAMEDestroy**](d3dxframedestroy.md), передав корневой узел иерархии Frame и объект производного класса [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6e7-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="5c6e7-161">[**Дестройфраме**](id3dxallocatehierarchy--destroyframe.md) и [**дестроймешконтаинер**](id3dxallocatehierarchy--destroymeshcontainer.md) будут вызываться для каждого объекта Frame и сетки в иерархии Frame.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="5c6e7-162">Ваша реализация **дестройфраме** должна освободить все, что выделено [**креатефраме**](id3dxallocatehierarchy--createframe.md), а также методы контейнера сетки.</span><span class="sxs-lookup"><span data-stu-id="5c6e7-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c6e7-163">Требования</span><span class="sxs-lookup"><span data-stu-id="5c6e7-163">Requirements</span></span>



| <span data-ttu-id="5c6e7-164">Требование</span><span class="sxs-lookup"><span data-stu-id="5c6e7-164">Requirement</span></span> | <span data-ttu-id="5c6e7-165">Значение</span><span class="sxs-lookup"><span data-stu-id="5c6e7-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6e7-166">Header</span><span class="sxs-lookup"><span data-stu-id="5c6e7-166">Header</span></span><br/>  | <dl> <span data-ttu-id="5c6e7-167"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c6e7-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5c6e7-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5c6e7-168">Library</span></span><br/> | <dl> <span data-ttu-id="5c6e7-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c6e7-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5c6e7-170">См. также</span><span class="sxs-lookup"><span data-stu-id="5c6e7-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6e7-171">Функции анимации</span><span class="sxs-lookup"><span data-stu-id="5c6e7-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
