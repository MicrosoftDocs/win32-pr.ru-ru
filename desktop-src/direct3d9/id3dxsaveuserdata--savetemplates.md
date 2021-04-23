---
description: Обратный вызов для пользователя при сохранении шаблона файла. x.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'Метод ID3DXSaveUserData:: Саветемплатес (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000510"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="eab4b-103">Метод ID3DXSaveUserData:: Саветемплатес</span><span class="sxs-lookup"><span data-stu-id="eab4b-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="eab4b-104">Обратный вызов для пользователя при сохранении шаблона файла. x.</span><span class="sxs-lookup"><span data-stu-id="eab4b-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eab4b-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="eab4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eab4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab4b-107">*пксофсаве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eab4b-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eab4b-108">Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="eab4b-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="eab4b-109">Указатель на файл. x сохранить объект.</span><span class="sxs-lookup"><span data-stu-id="eab4b-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="eab4b-110">Не используйте этот параметр для добавления объектов данных.</span><span class="sxs-lookup"><span data-stu-id="eab4b-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="eab4b-111">См. [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span><span class="sxs-lookup"><span data-stu-id="eab4b-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab4b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eab4b-112">Return value</span></span>

<span data-ttu-id="eab4b-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eab4b-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eab4b-114">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="eab4b-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="eab4b-115">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="eab4b-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="eab4b-116">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="eab4b-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab4b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eab4b-117">Remarks</span></span>

<span data-ttu-id="eab4b-118">[**ID3DXSaveUserData:: регистертемплатес**](id3dxsaveuserdata--registertemplates.md) и **ID3DXSaveUserData:: саветемплатес** предоставляют механизм для добавления шаблона в файл. x для сохранения пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="eab4b-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab4b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eab4b-119">Requirements</span></span>



| <span data-ttu-id="eab4b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eab4b-120">Requirement</span></span> | <span data-ttu-id="eab4b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eab4b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eab4b-122">Header</span><span class="sxs-lookup"><span data-stu-id="eab4b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="eab4b-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab4b-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="eab4b-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eab4b-124">Library</span></span><br/> | <dl> <span data-ttu-id="eab4b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eab4b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eab4b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eab4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab4b-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="eab4b-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
