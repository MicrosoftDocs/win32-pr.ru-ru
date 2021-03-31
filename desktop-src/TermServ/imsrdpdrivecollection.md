---
title: Интерфейс Имсрдпдривеколлектион
description: Представляет коллекцию объектов Drive.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, описание
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491628"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="b88f1-105">Интерфейс Имсрдпдривеколлектион</span><span class="sxs-lookup"><span data-stu-id="b88f1-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="b88f1-106">Представляет коллекцию объектов Drive.</span><span class="sxs-lookup"><span data-stu-id="b88f1-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="b88f1-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="b88f1-107">Members</span></span>

<span data-ttu-id="b88f1-108">Интерфейс **имсрдпдривеколлектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b88f1-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b88f1-109">**Имсрдпдривеколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b88f1-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="b88f1-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b88f1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b88f1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b88f1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b88f1-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b88f1-112">Methods</span></span>

<span data-ttu-id="b88f1-113">Интерфейс **имсрдпдривеколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b88f1-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="b88f1-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b88f1-114">Method</span></span>                                                     | <span data-ttu-id="b88f1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b88f1-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="b88f1-116">**рескандривес**</span><span class="sxs-lookup"><span data-stu-id="b88f1-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="b88f1-117">Обновляет список объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b88f1-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b88f1-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="b88f1-118">Properties</span></span>

<span data-ttu-id="b88f1-119">Интерфейс **имсрдпдривеколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b88f1-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="b88f1-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="b88f1-120">Property</span></span>                                                              | <span data-ttu-id="b88f1-121">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="b88f1-121">Access type</span></span>          | <span data-ttu-id="b88f1-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b88f1-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="b88f1-123">**дривебиндекс**</span><span class="sxs-lookup"><span data-stu-id="b88f1-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="b88f1-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b88f1-124">Read-only</span></span><br/> | <span data-ttu-id="b88f1-125">Извлекает диск по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="b88f1-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="b88f1-126">**дривекаунт**</span><span class="sxs-lookup"><span data-stu-id="b88f1-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="b88f1-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b88f1-127">Read-only</span></span><br/> | <span data-ttu-id="b88f1-128">Возвращает число объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b88f1-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b88f1-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b88f1-129">Requirements</span></span>



| <span data-ttu-id="b88f1-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b88f1-130">Requirement</span></span> | <span data-ttu-id="b88f1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b88f1-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b88f1-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b88f1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b88f1-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b88f1-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b88f1-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b88f1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b88f1-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b88f1-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b88f1-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b88f1-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="b88f1-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88f1-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b88f1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b88f1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b88f1-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b88f1-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b88f1-140">IID</span><span class="sxs-lookup"><span data-stu-id="b88f1-140">IID</span></span><br/>                      | <span data-ttu-id="b88f1-141">IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="b88f1-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b88f1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b88f1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b88f1-143">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="b88f1-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="b88f1-144">**имсрдпдриве**</span><span class="sxs-lookup"><span data-stu-id="b88f1-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

