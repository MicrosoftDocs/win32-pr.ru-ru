---
description: Приложения используют методы интерфейса Идиректксфилеобжект для получения сведений о файловых объектах Microsoft DirectX. Не рекомендуется.
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: Интерфейс Идиректксфилеобжект (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: e03f4a80c0cff25fa9416d35c20f2d60d17b206b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684990"
---
# <a name="idirectxfileobject-interface"></a><span data-ttu-id="05ed6-104">Интерфейс Идиректксфилеобжект</span><span class="sxs-lookup"><span data-stu-id="05ed6-104">IDirectXFileObject interface</span></span>

<span data-ttu-id="05ed6-105">Приложения используют методы интерфейса Идиректксфилеобжект для получения сведений о файловых объектах Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="05ed6-105">Applications use the methods of the IDirectXFileObject interface to retrieve information about Microsoft DirectX file objects.</span></span> <span data-ttu-id="05ed6-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="05ed6-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="05ed6-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="05ed6-107">Members</span></span>

<span data-ttu-id="05ed6-108">Интерфейс **идиректксфилеобжект** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="05ed6-108">The **IDirectXFileObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05ed6-109">**Идиректксфилеобжект** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="05ed6-109">**IDirectXFileObject** also has these types of members:</span></span>

-   [<span data-ttu-id="05ed6-110">Методы</span><span class="sxs-lookup"><span data-stu-id="05ed6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="05ed6-111">Методы</span><span class="sxs-lookup"><span data-stu-id="05ed6-111">Methods</span></span>

<span data-ttu-id="05ed6-112">Интерфейс **идиректксфилеобжект** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="05ed6-112">The **IDirectXFileObject** interface has these methods.</span></span>



| <span data-ttu-id="05ed6-113">Метод</span><span class="sxs-lookup"><span data-stu-id="05ed6-113">Method</span></span>                                         | <span data-ttu-id="05ed6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="05ed6-114">Description</span></span>                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05ed6-115">**GetId**</span><span class="sxs-lookup"><span data-stu-id="05ed6-115">**GetId**</span></span>](idirectxfileobject--getid.md)     | <span data-ttu-id="05ed6-116">Получает указатель на идентификатор GUID, определяющий объект файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="05ed6-116">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="05ed6-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="05ed6-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="05ed6-118">**GetName**</span><span class="sxs-lookup"><span data-stu-id="05ed6-118">**GetName**</span></span>](idirectxfileobject--getname.md) | <span data-ttu-id="05ed6-119">Получает указатель на имя объекта файла DirectX.</span><span class="sxs-lookup"><span data-stu-id="05ed6-119">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="05ed6-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="05ed6-120">Deprecated.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="05ed6-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05ed6-121">Remarks</span></span>

<span data-ttu-id="05ed6-122">Идентификатор GUID для интерфейса Идиректксфилеобжект — IID \_ идиректксфилеобжект.</span><span class="sxs-lookup"><span data-stu-id="05ed6-122">The GUID for the IDirectXFileObject interface is IID\_IDirectXFileObject.</span></span>

<span data-ttu-id="05ed6-123">Тип ЛПДИРЕКТКСФИЛЕОБЖЕКТ определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="05ed6-123">The LPDIRECTXFILEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="05ed6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="05ed6-124">Requirements</span></span>



| <span data-ttu-id="05ed6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="05ed6-125">Requirement</span></span> | <span data-ttu-id="05ed6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="05ed6-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05ed6-127">Header</span><span class="sxs-lookup"><span data-stu-id="05ed6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="05ed6-128"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="05ed6-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="05ed6-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05ed6-129">Library</span></span><br/> | <dl> <span data-ttu-id="05ed6-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05ed6-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ed6-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05ed6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ed6-132">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="05ed6-132">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
