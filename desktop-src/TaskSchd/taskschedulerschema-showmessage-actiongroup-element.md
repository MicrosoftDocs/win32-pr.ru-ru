---
title: ShowMessage (actionGroup), элемент
description: Представляет действие, показывающее окно сообщения.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- планировщик задач элемента ShowMessage
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340495"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="f2f3b-104">ShowMessage (actionGroup), элемент</span><span class="sxs-lookup"><span data-stu-id="f2f3b-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="f2f3b-105">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="f2f3b-106">Элемент **ShowMessage** определяется параметром [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f3b-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f2f3b-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f2f3b-107">Parent element</span></span>



| <span data-ttu-id="f2f3b-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="f2f3b-108">Element</span></span>                                                                    | <span data-ttu-id="f2f3b-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="f2f3b-109">Derived from</span></span>                                                       | <span data-ttu-id="f2f3b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f2f3b-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f2f3b-111">**Действия (taskType)**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="f2f3b-112">**актионстипе**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="f2f3b-113">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f2f3b-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f2f3b-114">Child elements</span></span>



| <span data-ttu-id="f2f3b-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="f2f3b-115">Element</span></span>                                                            | <span data-ttu-id="f2f3b-116">Тип</span><span class="sxs-lookup"><span data-stu-id="f2f3b-116">Type</span></span>           | <span data-ttu-id="f2f3b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f2f3b-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="f2f3b-118">**Текст**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="f2f3b-119">нонемптистринг</span><span class="sxs-lookup"><span data-stu-id="f2f3b-119">nonEmptyString</span></span> | <span data-ttu-id="f2f3b-120">Задает текст, отображаемый в тексте окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="f2f3b-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f2f3b-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="f2f3b-122">нонемптистринг</span><span class="sxs-lookup"><span data-stu-id="f2f3b-122">nonEmptyString</span></span> | <span data-ttu-id="f2f3b-123">Задает заголовок окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="f2f3b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2f3b-124">Remarks</span></span>

<span data-ttu-id="f2f3b-125">Для разработки сценариев действие окна сообщения указывается с помощью объекта [**шовмессажеактион**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="f2f3b-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="f2f3b-126">Для разработки на C++ действие окна сообщения указывается с помощью интерфейса [**ишовмессажеактион**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .</span><span class="sxs-lookup"><span data-stu-id="f2f3b-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="f2f3b-127">**Windows 8 и Windows Server 2012:** Этот элемент был удален.</span><span class="sxs-lookup"><span data-stu-id="f2f3b-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="f2f3b-128">Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="f2f3b-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="f2f3b-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="f2f3b-129">Examples</span></span>

<span data-ttu-id="f2f3b-130">Полный пример XML-кода для задачи, использующей действие окна сообщения, см. в разделе [Пример сообщения (XML)](/previous-versions//aa381917(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2f3b-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f3b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f2f3b-131">Requirements</span></span>



| <span data-ttu-id="f2f3b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f2f3b-132">Requirement</span></span> | <span data-ttu-id="f2f3b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f2f3b-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f2f3b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2f3b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f2f3b-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2f3b-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f2f3b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2f3b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f2f3b-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f2f3b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f2f3b-138">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f2f3b-138">End of client support</span></span><br/>    | <span data-ttu-id="f2f3b-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2f3b-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="f2f3b-140">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f2f3b-140">End of server support</span></span><br/>    | <span data-ttu-id="f2f3b-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2f3b-141">Windows Server 2008 R2</span></span><br/>                    |



 

