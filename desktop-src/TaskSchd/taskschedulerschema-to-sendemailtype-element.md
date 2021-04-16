---
title: To (Сендемаилтипе), элемент
description: Содержит адреса электронной почты, на которые будет отправлено электронное письмо.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- В элемент планировщик задач
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672527"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="59246-104">To (Сендемаилтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="59246-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="59246-105">Содержит адреса электронной почты, на которые будет отправлено электронное письмо.</span><span class="sxs-lookup"><span data-stu-id="59246-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="59246-106">Элемент **to** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="59246-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="59246-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="59246-107">Parent element</span></span>



| <span data-ttu-id="59246-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="59246-108">Element</span></span>                                                                              | <span data-ttu-id="59246-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="59246-109">Derived from</span></span>                                                           | <span data-ttu-id="59246-110">Описание</span><span class="sxs-lookup"><span data-stu-id="59246-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="59246-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="59246-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="59246-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="59246-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="59246-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="59246-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="59246-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59246-114">Remarks</span></span>

<span data-ttu-id="59246-115">Сведения о разработке на языке C++ см. [**в разделе свойство объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span><span class="sxs-lookup"><span data-stu-id="59246-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="59246-116">Сведения о разработке сценариев см. в разделе [**EmailAction.to**](emailaction-to.md).</span><span class="sxs-lookup"><span data-stu-id="59246-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59246-117">Требования</span><span class="sxs-lookup"><span data-stu-id="59246-117">Requirements</span></span>



| <span data-ttu-id="59246-118">Требование</span><span class="sxs-lookup"><span data-stu-id="59246-118">Requirement</span></span> | <span data-ttu-id="59246-119">Значение</span><span class="sxs-lookup"><span data-stu-id="59246-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59246-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59246-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59246-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59246-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59246-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59246-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59246-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59246-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





