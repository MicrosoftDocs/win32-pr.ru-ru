---
description: Загрузка дочерних данных фрейма из файла. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'Метод ID3DXLoadUserData:: Лоадфрамечилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53bde98f0e756fd1baff4c509179f15e8489e74f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548103"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a><span data-ttu-id="cda36-103">Метод ID3DXLoadUserData:: Лоадфрамечилддата</span><span class="sxs-lookup"><span data-stu-id="cda36-103">ID3DXLoadUserData::LoadFrameChildData method</span></span>

<span data-ttu-id="cda36-104">Загрузка дочерних данных фрейма из файла. x.</span><span class="sxs-lookup"><span data-stu-id="cda36-104">Load frame child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda36-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cda36-105">Syntax</span></span>


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="cda36-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cda36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda36-107">*пфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cda36-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda36-108">Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="cda36-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="cda36-109">Указатель на контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="cda36-109">Pointer to a mesh container.</span></span> <span data-ttu-id="cda36-110">См. [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="cda36-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cda36-111">*пксофчилддата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cda36-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cda36-112">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="cda36-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="cda36-113">Указатель на структуру данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="cda36-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="cda36-114">Это определено в Дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="cda36-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda36-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cda36-115">Return value</span></span>

<span data-ttu-id="cda36-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cda36-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cda36-117">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="cda36-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="cda36-118">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="cda36-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="cda36-119">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="cda36-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda36-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cda36-120">Requirements</span></span>



| <span data-ttu-id="cda36-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cda36-121">Requirement</span></span> | <span data-ttu-id="cda36-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cda36-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cda36-123">Header</span><span class="sxs-lookup"><span data-stu-id="cda36-123">Header</span></span><br/>  | <dl> <span data-ttu-id="cda36-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda36-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cda36-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cda36-125">Library</span></span><br/> | <dl> <span data-ttu-id="cda36-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cda36-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cda36-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cda36-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda36-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="cda36-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




