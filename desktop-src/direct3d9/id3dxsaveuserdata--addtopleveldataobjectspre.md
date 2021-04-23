---
description: Добавьте объект верхнего уровня перед иерархией Frame.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'Метод ID3DXSaveUserData:: Аддтоплевелдатаобжектспре (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664999"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a><span data-ttu-id="3cba4-103">Метод ID3DXSaveUserData:: Аддтоплевелдатаобжектспре</span><span class="sxs-lookup"><span data-stu-id="3cba4-103">ID3DXSaveUserData::AddTopLevelDataObjectsPre method</span></span>

<span data-ttu-id="3cba4-104">Добавьте объект верхнего уровня перед иерархией Frame.</span><span class="sxs-lookup"><span data-stu-id="3cba4-104">Add a top level object before the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cba4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cba4-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="3cba4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cba4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cba4-107">*пксофсаве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3cba4-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cba4-108">Тип: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="3cba4-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="3cba4-109">Указатель на файл. x сохранить объект.</span><span class="sxs-lookup"><span data-stu-id="3cba4-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="3cba4-110">Используйте этот указатель для вызова [**идиректксфилесавеобжект:: креатедатаобжект**](idirectxfilesaveobject--createdataobject.md) , чтобы создать объект данных для сохранения.</span><span class="sxs-lookup"><span data-stu-id="3cba4-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="3cba4-111">Затем вызовите метод [**идиректксфилесавеобжект:: SaveData**](idirectxfilesaveobject--savedata.md) , чтобы сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="3cba4-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cba4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cba4-112">Return value</span></span>

<span data-ttu-id="3cba4-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3cba4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3cba4-114">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="3cba4-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="3cba4-115">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="3cba4-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="3cba4-116">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md), так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="3cba4-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cba4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3cba4-117">Requirements</span></span>



| <span data-ttu-id="3cba4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3cba4-118">Requirement</span></span> | <span data-ttu-id="3cba4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3cba4-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cba4-120">Header</span><span class="sxs-lookup"><span data-stu-id="3cba4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3cba4-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cba4-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3cba4-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3cba4-122">Library</span></span><br/> | <dl> <span data-ttu-id="3cba4-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cba4-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3cba4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cba4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cba4-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="3cba4-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 
