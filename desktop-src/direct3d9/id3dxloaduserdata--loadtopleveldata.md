---
description: Загрузка данных верхнего уровня из файла. x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'Метод ID3DXLoadUserData:: Лоадтоплевелдата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713937"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="6f077-103">Метод ID3DXLoadUserData:: Лоадтоплевелдата</span><span class="sxs-lookup"><span data-stu-id="6f077-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="6f077-104">Загрузка данных верхнего уровня из файла. x.</span><span class="sxs-lookup"><span data-stu-id="6f077-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f077-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f077-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="6f077-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f077-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f077-107">*пксофчилддата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f077-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f077-108">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="6f077-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="6f077-109">Указатель на структуру данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="6f077-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="6f077-110">Это определено в Дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="6f077-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f077-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f077-111">Return value</span></span>

<span data-ttu-id="6f077-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f077-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f077-113">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="6f077-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="6f077-114">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6f077-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="6f077-115">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="6f077-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f077-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6f077-116">Requirements</span></span>



| <span data-ttu-id="6f077-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6f077-117">Requirement</span></span> | <span data-ttu-id="6f077-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6f077-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f077-119">Header</span><span class="sxs-lookup"><span data-stu-id="6f077-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6f077-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f077-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6f077-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f077-121">Library</span></span><br/> | <dl> <span data-ttu-id="6f077-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f077-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f077-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f077-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f077-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="6f077-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




