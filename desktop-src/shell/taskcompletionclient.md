---
description: Включает выполнение задачи.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Интерфейс Тасккомплетионклиент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266163"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="d714b-103">Интерфейс Тасккомплетионклиент</span><span class="sxs-lookup"><span data-stu-id="d714b-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="d714b-104">Включает выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="d714b-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="d714b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="d714b-105">Members</span></span>

<span data-ttu-id="d714b-106">Интерфейс **тасккомплетионклиент** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d714b-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d714b-107">**Тасккомплетионклиент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d714b-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="d714b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="d714b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d714b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d714b-109">Methods</span></span>

<span data-ttu-id="d714b-110">Интерфейс **тасккомплетионклиент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d714b-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="d714b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="d714b-111">Method</span></span>                                                                    | <span data-ttu-id="d714b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d714b-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="d714b-113">**апплитасккомплетион**</span><span class="sxs-lookup"><span data-stu-id="d714b-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="d714b-114">Начинает выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="d714b-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="d714b-115">**ревокетасккомплетион**</span><span class="sxs-lookup"><span data-stu-id="d714b-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="d714b-116">Завершает выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="d714b-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="d714b-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d714b-117">Remarks</span></span>

<span data-ttu-id="d714b-118">Идентификатор GUID для этого интерфейса — "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span><span class="sxs-lookup"><span data-stu-id="d714b-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="d714b-119">Этот API является устаревшим и может быть недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="d714b-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="d714b-120">Вместо этого приложения должны использовать API-интерфейсы в пространстве имен [**Windows. ApplicationModel. екстендедексекутион**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="d714b-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="d714b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d714b-121">Requirements</span></span>



| <span data-ttu-id="d714b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d714b-122">Requirement</span></span> | <span data-ttu-id="d714b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d714b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d714b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d714b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d714b-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d714b-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d714b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d714b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d714b-127">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="d714b-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d714b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d714b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d714b-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d714b-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
