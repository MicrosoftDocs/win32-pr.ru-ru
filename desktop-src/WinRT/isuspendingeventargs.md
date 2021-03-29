---
description: Предоставляет данные для события приостановки приложения.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Интерфейс Исуспендинжевентаргс (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647169"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="3a81f-103">Интерфейс Исуспендинжевентаргс</span><span class="sxs-lookup"><span data-stu-id="3a81f-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="3a81f-104">Предоставляет данные для события приостановки приложения.</span><span class="sxs-lookup"><span data-stu-id="3a81f-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="3a81f-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="3a81f-105">Members</span></span>

<span data-ttu-id="3a81f-106">Интерфейс **исуспендинжевентаргс** наследует от [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="3a81f-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="3a81f-107">**Исуспендинжевентаргс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3a81f-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="3a81f-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a81f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a81f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a81f-109">Properties</span></span>

<span data-ttu-id="3a81f-110">Интерфейс **исуспендинжевентаргс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3a81f-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="3a81f-111">Свойство</span><span class="sxs-lookup"><span data-stu-id="3a81f-111">Property</span></span>                                                                           | <span data-ttu-id="3a81f-112">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3a81f-112">Access type</span></span>           | <span data-ttu-id="3a81f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3a81f-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="3a81f-114">**суспендингоператион**</span><span class="sxs-lookup"><span data-stu-id="3a81f-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="3a81f-115">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="3a81f-115">Read/write</span></span><br/> | <span data-ttu-id="3a81f-116">Возвращает операцию приостановки приложения.</span><span class="sxs-lookup"><span data-stu-id="3a81f-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a81f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a81f-117">Remarks</span></span>

<span data-ttu-id="3a81f-118">Доступ к этому объекту осуществляется при реализации таких обработчиков событий, как [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), и [**Добавление \_ приостановки**](/previous-versions//hh438376(v=vs.85)) для реагирования на события приостановки приложения.</span><span class="sxs-lookup"><span data-stu-id="3a81f-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a81f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3a81f-119">Requirements</span></span>



| <span data-ttu-id="3a81f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3a81f-120">Requirement</span></span> | <span data-ttu-id="3a81f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3a81f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a81f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a81f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3a81f-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3a81f-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3a81f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a81f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3a81f-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3a81f-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3a81f-126">Header</span><span class="sxs-lookup"><span data-stu-id="3a81f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a81f-127"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a81f-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a81f-128">IDL</span><span class="sxs-lookup"><span data-stu-id="3a81f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a81f-129"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a81f-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a81f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a81f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a81f-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="3a81f-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="3a81f-132">**исуспендингоператион**</span><span class="sxs-lookup"><span data-stu-id="3a81f-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="3a81f-133">**исуспендингдеферрал**</span><span class="sxs-lookup"><span data-stu-id="3a81f-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 
