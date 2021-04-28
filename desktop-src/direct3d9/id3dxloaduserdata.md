---
description: Интерфейс ID3DXLoadUserData. Этот интерфейс реализуется приложением для сохранения дополнительных пользовательских данных, внедренных в файлы. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Интерфейс ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83d603d2ec5fde00ef0b29d84368e04a1276f992
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093632"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="9b765-103">Интерфейс ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="9b765-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="9b765-104">Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x.</span><span class="sxs-lookup"><span data-stu-id="9b765-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="9b765-105">Экземпляр этого интерфейса передается в [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), и D3DX вызывает соответствующий метод для этого интерфейса каждый раз при обнаружении соответствующих данных.</span><span class="sxs-lookup"><span data-stu-id="9b765-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="9b765-106">Например, для каждого объекта Frame в файле. x вызывается [**ID3DXLoadUserData:: лоадфрамечилддата**](id3dxloaduserdata--loadframechilddata.md) и ему передаются дочерние данные.</span><span class="sxs-lookup"><span data-stu-id="9b765-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="9b765-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="9b765-107">Members</span></span>

<span data-ttu-id="9b765-108">Интерфейс **ID3DXLoadUserData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9b765-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9b765-109">**ID3DXLoadUserData** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9b765-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="9b765-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9b765-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9b765-111">Методы</span><span class="sxs-lookup"><span data-stu-id="9b765-111">Methods</span></span>

<span data-ttu-id="9b765-112">Интерфейс **ID3DXLoadUserData** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9b765-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="9b765-113">Метод</span><span class="sxs-lookup"><span data-stu-id="9b765-113">Method</span></span>                                                              | <span data-ttu-id="9b765-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9b765-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="9b765-115">**лоадфрамечилддата**</span><span class="sxs-lookup"><span data-stu-id="9b765-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="9b765-116">Загрузка дочерних данных фрейма из файла. x.</span><span class="sxs-lookup"><span data-stu-id="9b765-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="9b765-117">**лоадмешчилддата**</span><span class="sxs-lookup"><span data-stu-id="9b765-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="9b765-118">Загрузка дочерних данных сетки из файла. x.</span><span class="sxs-lookup"><span data-stu-id="9b765-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="9b765-119">**лоадтоплевелдата**</span><span class="sxs-lookup"><span data-stu-id="9b765-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="9b765-120">Загрузка данных верхнего уровня из файла. x.</span><span class="sxs-lookup"><span data-stu-id="9b765-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="9b765-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b765-121">Remarks</span></span>

<span data-ttu-id="9b765-122">Тип LPD3DXLOADUSERDATA определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="9b765-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="9b765-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9b765-123">Requirements</span></span>



| <span data-ttu-id="9b765-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9b765-124">Requirement</span></span> | <span data-ttu-id="9b765-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9b765-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b765-126">Header</span><span class="sxs-lookup"><span data-stu-id="9b765-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9b765-127"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b765-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9b765-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9b765-128">Library</span></span><br/> | <dl> <span data-ttu-id="9b765-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9b765-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9b765-130">См. также</span><span class="sxs-lookup"><span data-stu-id="9b765-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b765-131">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="9b765-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
