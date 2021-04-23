---
description: Представляет метод, который вызывается при завершении асинхронного действия.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Интерфейс Асинкактионкомплетедхандлер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711063"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="ed601-103">Интерфейс Асинкактионкомплетедхандлер</span><span class="sxs-lookup"><span data-stu-id="ed601-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="ed601-104">Представляет метод, который вызывается при завершении асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="ed601-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="ed601-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="ed601-105">Members</span></span>

<span data-ttu-id="ed601-106">Интерфейс **асинкактионкомплетедхандлер** наследует от [**иасинЦинфо**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span><span class="sxs-lookup"><span data-stu-id="ed601-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="ed601-107">**Асинкактионкомплетедхандлер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed601-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="ed601-108">Методы</span><span class="sxs-lookup"><span data-stu-id="ed601-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ed601-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ed601-109">Methods</span></span>

<span data-ttu-id="ed601-110">Интерфейс **асинкактионкомплетедхандлер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ed601-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="ed601-111">Метод</span><span class="sxs-lookup"><span data-stu-id="ed601-111">Method</span></span>                                               | <span data-ttu-id="ed601-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ed601-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed601-113">**Вызвать**</span><span class="sxs-lookup"><span data-stu-id="ed601-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="ed601-114">Вызывает метод, вызываемый при завершении указанного асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="ed601-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed601-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed601-115">Remarks</span></span>

<span data-ttu-id="ed601-116">Назначьте **Асинкактионкомплетедхандлер** [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) , чтобы получить уведомление о завершении асинхронного действия.</span><span class="sxs-lookup"><span data-stu-id="ed601-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed601-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ed601-117">Requirements</span></span>



| <span data-ttu-id="ed601-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ed601-118">Requirement</span></span> | <span data-ttu-id="ed601-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ed601-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed601-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed601-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed601-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ed601-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="ed601-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed601-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed601-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed601-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="ed601-124">Header</span><span class="sxs-lookup"><span data-stu-id="ed601-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed601-125"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed601-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed601-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed601-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed601-127">**иасинЦинфо**</span><span class="sxs-lookup"><span data-stu-id="ed601-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

