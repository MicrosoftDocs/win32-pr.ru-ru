---
title: ReplyTo (Сендемаилтипе), элемент
description: Содержит адреса электронной почты, на которые дан ответ в сообщении электронной почты.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- Элемент ReplyTo планировщик задач
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137683"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="cd63d-104">ReplyTo (Сендемаилтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="cd63d-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="cd63d-105">Содержит адреса электронной почты, на которые дан ответ в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cd63d-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="cd63d-106">Элемент **ReplyTo** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd63d-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cd63d-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cd63d-107">Parent element</span></span>



| <span data-ttu-id="cd63d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cd63d-108">Element</span></span>                                                                              | <span data-ttu-id="cd63d-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="cd63d-109">Derived from</span></span>                                                           | <span data-ttu-id="cd63d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cd63d-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="cd63d-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="cd63d-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="cd63d-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="cd63d-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="cd63d-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cd63d-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cd63d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd63d-114">Remarks</span></span>

<span data-ttu-id="cd63d-115">Сведения о разработке с + + см. в разделе [**Свойство ReplyTo объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span><span class="sxs-lookup"><span data-stu-id="cd63d-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="cd63d-116">Сведения о разработке сценариев см. в разделе [**емаилактион. ReplyTo**](emailaction-replyto.md).</span><span class="sxs-lookup"><span data-stu-id="cd63d-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd63d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cd63d-117">Requirements</span></span>



| <span data-ttu-id="cd63d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cd63d-118">Requirement</span></span> | <span data-ttu-id="cd63d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cd63d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd63d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd63d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd63d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd63d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd63d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd63d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd63d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd63d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





