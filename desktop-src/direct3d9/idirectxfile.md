---
description: Приложения используют методы интерфейса Идиректксфиле для создания экземпляров интерфейсов Идиректксфилинумобжект и Идиректксфилесавеобжект, а также для регистрации шаблонов. Не рекомендуется.
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: Интерфейс Идиректксфиле (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914795"
---
# <a name="idirectxfile-interface"></a><span data-ttu-id="252bb-104">Интерфейс Идиректксфиле</span><span class="sxs-lookup"><span data-stu-id="252bb-104">IDirectXFile interface</span></span>

<span data-ttu-id="252bb-105">Приложения используют методы интерфейса Идиректксфиле для создания экземпляров интерфейсов [**идиректксфилинумобжект**](idirectxfileenumobject.md) и [**идиректксфилесавеобжект**](idirectxfilesaveobject.md) , а также для регистрации шаблонов.</span><span class="sxs-lookup"><span data-stu-id="252bb-105">Applications use the methods of the IDirectXFile interface to create instances of the [**IDirectXFileEnumObject**](idirectxfileenumobject.md) and [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interfaces, and to register templates.</span></span> <span data-ttu-id="252bb-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="252bb-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="252bb-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="252bb-107">Members</span></span>

<span data-ttu-id="252bb-108">Интерфейс **идиректксфиле** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="252bb-108">The **IDirectXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="252bb-109">**Идиректксфиле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="252bb-109">**IDirectXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="252bb-110">Методы</span><span class="sxs-lookup"><span data-stu-id="252bb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="252bb-111">Методы</span><span class="sxs-lookup"><span data-stu-id="252bb-111">Methods</span></span>

<span data-ttu-id="252bb-112">Интерфейс **идиректксфиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="252bb-112">The **IDirectXFile** interface has these methods.</span></span>



| <span data-ttu-id="252bb-113">Метод</span><span class="sxs-lookup"><span data-stu-id="252bb-113">Method</span></span>                                                       | <span data-ttu-id="252bb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="252bb-114">Description</span></span>                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="252bb-115">**креатинумобжект**</span><span class="sxs-lookup"><span data-stu-id="252bb-115">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)   | <span data-ttu-id="252bb-116">Создает объект перечислителя.</span><span class="sxs-lookup"><span data-stu-id="252bb-116">Creates an enumerator object.</span></span> <span data-ttu-id="252bb-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="252bb-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="252bb-118">**креатесавеобжект**</span><span class="sxs-lookup"><span data-stu-id="252bb-118">**CreateSaveObject**</span></span>](idirectxfile--createsaveobject.md)   | <span data-ttu-id="252bb-119">Создает объект Save.</span><span class="sxs-lookup"><span data-stu-id="252bb-119">Creates a save object.</span></span> <span data-ttu-id="252bb-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="252bb-120">Deprecated.</span></span><br/>        |
| [<span data-ttu-id="252bb-121">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="252bb-121">**RegisterTemplates**</span></span>](idirectxfile--registertemplates.md) | <span data-ttu-id="252bb-122">Регистрирует пользовательские шаблоны.</span><span class="sxs-lookup"><span data-stu-id="252bb-122">Registers custom templates.</span></span> <span data-ttu-id="252bb-123">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="252bb-123">Deprecated.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="252bb-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="252bb-124">Remarks</span></span>

<span data-ttu-id="252bb-125">Глобальный уникальный идентификатор (GUID) для интерфейса Идиректксфиле — IID \_ идиректксфиле.</span><span class="sxs-lookup"><span data-stu-id="252bb-125">The globally unique identifier (GUID) for the IDirectXFile interface is IID\_IDirectXFile.</span></span>

<span data-ttu-id="252bb-126">Интерфейс Идиректксфиле получается путем вызова функции [**директксфилекреате**](directxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="252bb-126">The IDirectXFile interface is obtained by calling the [**DirectXFileCreate**](directxfilecreate.md) function.</span></span>

<span data-ttu-id="252bb-127">Тип ЛПДИРЕКТКСФИЛЕ определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="252bb-127">The LPDIRECTXFILE type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFile *LPDIRECTXFILE;
```



## <a name="requirements"></a><span data-ttu-id="252bb-128">Требования</span><span class="sxs-lookup"><span data-stu-id="252bb-128">Requirements</span></span>



| <span data-ttu-id="252bb-129">Требование</span><span class="sxs-lookup"><span data-stu-id="252bb-129">Requirement</span></span> | <span data-ttu-id="252bb-130">Значение</span><span class="sxs-lookup"><span data-stu-id="252bb-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="252bb-131">Header</span><span class="sxs-lookup"><span data-stu-id="252bb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="252bb-132"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="252bb-132"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="252bb-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="252bb-133">Library</span></span><br/> | <dl> <span data-ttu-id="252bb-134"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="252bb-134"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="252bb-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="252bb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="252bb-136">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="252bb-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
