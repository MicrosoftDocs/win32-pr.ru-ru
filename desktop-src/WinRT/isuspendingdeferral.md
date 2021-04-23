---
description: Управляет отложенной операцией приостановки приложения.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Интерфейс Исуспендингдеферрал (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647170"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="97133-103">Интерфейс Исуспендингдеферрал</span><span class="sxs-lookup"><span data-stu-id="97133-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="97133-104">Управляет отложенной операцией приостановки приложения.</span><span class="sxs-lookup"><span data-stu-id="97133-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="97133-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="97133-105">Members</span></span>

<span data-ttu-id="97133-106">Интерфейс **исуспендингдеферрал** наследует от [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="97133-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="97133-107">**Исуспендингдеферрал** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97133-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="97133-108">Методы</span><span class="sxs-lookup"><span data-stu-id="97133-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97133-109">Методы</span><span class="sxs-lookup"><span data-stu-id="97133-109">Methods</span></span>

<span data-ttu-id="97133-110">Интерфейс **исуспендингдеферрал** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="97133-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="97133-111">Метод</span><span class="sxs-lookup"><span data-stu-id="97133-111">Method</span></span>                                           | <span data-ttu-id="97133-112">Описание</span><span class="sxs-lookup"><span data-stu-id="97133-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97133-113">**Завершить**</span><span class="sxs-lookup"><span data-stu-id="97133-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="97133-114">Уведомляет систему, что приложение сохранило свои данные и готово к приостановке.</span><span class="sxs-lookup"><span data-stu-id="97133-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="97133-115">Требования</span><span class="sxs-lookup"><span data-stu-id="97133-115">Requirements</span></span>



| <span data-ttu-id="97133-116">Требование</span><span class="sxs-lookup"><span data-stu-id="97133-116">Requirement</span></span> | <span data-ttu-id="97133-117">Значение</span><span class="sxs-lookup"><span data-stu-id="97133-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97133-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97133-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97133-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97133-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="97133-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97133-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97133-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97133-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97133-122">Header</span><span class="sxs-lookup"><span data-stu-id="97133-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="97133-123"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="97133-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="97133-124">IDL</span><span class="sxs-lookup"><span data-stu-id="97133-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97133-125"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97133-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97133-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97133-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97133-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="97133-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="97133-128">**исуспендинжевентаргс**</span><span class="sxs-lookup"><span data-stu-id="97133-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="97133-129">**исуспендингоператион**</span><span class="sxs-lookup"><span data-stu-id="97133-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 
