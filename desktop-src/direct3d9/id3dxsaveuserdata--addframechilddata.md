---
description: Добавьте дочерние данные в рамку.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'Метод ID3DXSaveUserData:: Аддфрамечилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273950"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="efffa-103">Метод ID3DXSaveUserData:: Аддфрамечилддата</span><span class="sxs-lookup"><span data-stu-id="efffa-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="efffa-104">Добавьте дочерние данные в рамку.</span><span class="sxs-lookup"><span data-stu-id="efffa-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="efffa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efffa-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="efffa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efffa-107">*пфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efffa-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efffa-108">Тип: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="efffa-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="efffa-109">Указатель на контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="efffa-109">Pointer to a mesh container.</span></span> <span data-ttu-id="efffa-110">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="efffa-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="efffa-111">*пксофсаве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efffa-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efffa-112">Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="efffa-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="efffa-113">Указатель на файл. x сохранить объект.</span><span class="sxs-lookup"><span data-stu-id="efffa-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="efffa-114">Используйте указатель для вызова [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md) , чтобы добавить дочерний объект данных.</span><span class="sxs-lookup"><span data-stu-id="efffa-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="efffa-115">Не сохраняйте данные с помощью [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="efffa-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="efffa-116">*пксоффрамедата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efffa-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efffa-117">Тип: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="efffa-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="efffa-118">Указатель на узел данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="efffa-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="efffa-119">Используйте указатель для вызова [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) , чтобы добавить дочерний объект данных.</span><span class="sxs-lookup"><span data-stu-id="efffa-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efffa-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efffa-120">Return value</span></span>

<span data-ttu-id="efffa-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efffa-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efffa-122">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="efffa-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="efffa-123">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="efffa-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="efffa-124">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="efffa-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="efffa-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efffa-125">Remarks</span></span>

<span data-ttu-id="efffa-126">[**ID3DXSaveUserData:: регистертемплатес**](id3dxsaveuserdata--registertemplates.md) и [**ID3DXSaveUserData:: саветемплатес**](id3dxsaveuserdata--savetemplates.md) предоставляют механизм для добавления шаблона в файл. x для сохранения пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="efffa-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="efffa-127">Требования</span><span class="sxs-lookup"><span data-stu-id="efffa-127">Requirements</span></span>



| <span data-ttu-id="efffa-128">Требование</span><span class="sxs-lookup"><span data-stu-id="efffa-128">Requirement</span></span> | <span data-ttu-id="efffa-129">Значение</span><span class="sxs-lookup"><span data-stu-id="efffa-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efffa-130">Header</span><span class="sxs-lookup"><span data-stu-id="efffa-130">Header</span></span><br/>  | <dl> <span data-ttu-id="efffa-131"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="efffa-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="efffa-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="efffa-132">Library</span></span><br/> | <dl> <span data-ttu-id="efffa-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efffa-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="efffa-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efffa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efffa-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="efffa-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
