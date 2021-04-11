---
description: Добавление дочерних данных в сетку.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'Метод ID3DXSaveUserData:: Аддмешчилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273949"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a><span data-ttu-id="57f9b-103">Метод ID3DXSaveUserData:: Аддмешчилддата</span><span class="sxs-lookup"><span data-stu-id="57f9b-103">ID3DXSaveUserData::AddMeshChildData method</span></span>

<span data-ttu-id="57f9b-104">Добавление дочерних данных в сетку.</span><span class="sxs-lookup"><span data-stu-id="57f9b-104">Add child data to the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f9b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57f9b-105">Syntax</span></span>


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a><span data-ttu-id="57f9b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57f9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f9b-107">*пмешконтаинер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57f9b-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f9b-108">Тип: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***</span><span class="sxs-lookup"><span data-stu-id="57f9b-108">Type: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="57f9b-109">Указатель на контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="57f9b-109">Pointer to a mesh container.</span></span> <span data-ttu-id="57f9b-110">См. [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="57f9b-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="57f9b-111">*пксофсаве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57f9b-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f9b-112">Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="57f9b-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="57f9b-113">Указатель на файл. x сохранить объект.</span><span class="sxs-lookup"><span data-stu-id="57f9b-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="57f9b-114">Используйте указатель для вызова [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md) , чтобы добавить дочерний объект данных.</span><span class="sxs-lookup"><span data-stu-id="57f9b-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="57f9b-115">Не сохраняйте данные с помощью [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="57f9b-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="57f9b-116">*пксофмешдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57f9b-116">*pXofMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f9b-117">Тип: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="57f9b-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="57f9b-118">Указатель на узел данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="57f9b-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="57f9b-119">Используйте указатель для вызова [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) , чтобы добавить дочерний объект данных.</span><span class="sxs-lookup"><span data-stu-id="57f9b-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f9b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57f9b-120">Return value</span></span>

<span data-ttu-id="57f9b-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57f9b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57f9b-122">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="57f9b-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="57f9b-123">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="57f9b-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="57f9b-124">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="57f9b-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f9b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="57f9b-125">Requirements</span></span>



| <span data-ttu-id="57f9b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="57f9b-126">Requirement</span></span> | <span data-ttu-id="57f9b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="57f9b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57f9b-128">Header</span><span class="sxs-lookup"><span data-stu-id="57f9b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="57f9b-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="57f9b-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="57f9b-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57f9b-130">Library</span></span><br/> | <dl> <span data-ttu-id="57f9b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57f9b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57f9b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57f9b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f9b-133">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="57f9b-133">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
