---
description: Загрузка дочерних данных сетки из файла. x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'Метод ID3DXLoadUserData:: Лоадмешчилддата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713562"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a><span data-ttu-id="0c511-103">Метод ID3DXLoadUserData:: Лоадмешчилддата</span><span class="sxs-lookup"><span data-stu-id="0c511-103">ID3DXLoadUserData::LoadMeshChildData method</span></span>

<span data-ttu-id="0c511-104">Загрузка дочерних данных сетки из файла. x.</span><span class="sxs-lookup"><span data-stu-id="0c511-104">Load mesh child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c511-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c511-105">Syntax</span></span>


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="0c511-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c511-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c511-107">*пмешконтаинер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c511-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c511-108">Тип: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="0c511-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="0c511-109">Указатель на контейнер сетки.</span><span class="sxs-lookup"><span data-stu-id="0c511-109">Pointer to a mesh container.</span></span> <span data-ttu-id="0c511-110">См. [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0c511-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c511-111">*пксофчилддата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c511-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c511-112">Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="0c511-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="0c511-113">Указатель на структуру данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="0c511-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="0c511-114">Это определено в Дксфиле. h.</span><span class="sxs-lookup"><span data-stu-id="0c511-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c511-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c511-115">Return value</span></span>

<span data-ttu-id="0c511-116">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0c511-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0c511-117">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="0c511-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0c511-118">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0c511-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0c511-119">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке от D3DERR или D3DXERR, так как это приведет к сбою [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) и возврату ошибки.</span><span class="sxs-lookup"><span data-stu-id="0c511-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c511-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0c511-120">Requirements</span></span>



| <span data-ttu-id="0c511-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0c511-121">Requirement</span></span> | <span data-ttu-id="0c511-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0c511-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c511-123">Header</span><span class="sxs-lookup"><span data-stu-id="0c511-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0c511-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c511-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0c511-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0c511-125">Library</span></span><br/> | <dl> <span data-ttu-id="0c511-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c511-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c511-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c511-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c511-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="0c511-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




