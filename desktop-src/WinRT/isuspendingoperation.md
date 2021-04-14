---
description: Предоставляет сведения о приостановке работы приложения.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Интерфейс Исуспендингоператион (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541655"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="9657d-103">Интерфейс Исуспендингоператион</span><span class="sxs-lookup"><span data-stu-id="9657d-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="9657d-104">Предоставляет сведения о приостановке работы приложения.</span><span class="sxs-lookup"><span data-stu-id="9657d-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="9657d-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="9657d-105">Members</span></span>

<span data-ttu-id="9657d-106">Интерфейс **исуспендингоператион** наследует от [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="9657d-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="9657d-107">**Исуспендингоператион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9657d-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="9657d-108">Методы</span><span class="sxs-lookup"><span data-stu-id="9657d-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="9657d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="9657d-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9657d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="9657d-110">Methods</span></span>

<span data-ttu-id="9657d-111">Интерфейс **исуспендингоператион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9657d-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="9657d-112">Метод</span><span class="sxs-lookup"><span data-stu-id="9657d-112">Method</span></span>                                                  | <span data-ttu-id="9657d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="9657d-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="9657d-114">**РБП**</span><span class="sxs-lookup"><span data-stu-id="9657d-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="9657d-115">Запрашивает задержку операции приостановки выполнения приложения.</span><span class="sxs-lookup"><span data-stu-id="9657d-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9657d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="9657d-116">Properties</span></span>

<span data-ttu-id="9657d-117">Интерфейс **исуспендингоператион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9657d-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="9657d-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="9657d-118">Property</span></span>                                                     | <span data-ttu-id="9657d-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="9657d-119">Access type</span></span>           | <span data-ttu-id="9657d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="9657d-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="9657d-121">**Крайний срок**</span><span class="sxs-lookup"><span data-stu-id="9657d-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="9657d-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9657d-122">Read/write</span></span><br/> | <span data-ttu-id="9657d-123">Возвращает время, оставшееся до того, как будет продолжаться операция приостановки отложенного приложения.</span><span class="sxs-lookup"><span data-stu-id="9657d-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9657d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9657d-124">Requirements</span></span>



| <span data-ttu-id="9657d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9657d-125">Requirement</span></span> | <span data-ttu-id="9657d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9657d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9657d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9657d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9657d-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9657d-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9657d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9657d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9657d-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9657d-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9657d-131">Header</span><span class="sxs-lookup"><span data-stu-id="9657d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9657d-132"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="9657d-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="9657d-133">IDL</span><span class="sxs-lookup"><span data-stu-id="9657d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9657d-134"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9657d-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9657d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9657d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9657d-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="9657d-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="9657d-137">**исуспендингдеферрал**</span><span class="sxs-lookup"><span data-stu-id="9657d-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="9657d-138">**исуспендинжевентаргс**</span><span class="sxs-lookup"><span data-stu-id="9657d-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 
