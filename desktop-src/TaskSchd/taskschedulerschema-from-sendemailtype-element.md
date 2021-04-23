---
title: From (Сендемаилтипе), элемент
description: Содержит адрес электронной почты отправителя электронной почты.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Из планировщик задач элемента
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071410"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="8b1da-104">From (Сендемаилтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="8b1da-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="8b1da-105">Содержит адрес электронной почты отправителя электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8b1da-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="8b1da-106">Элемент **from** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8b1da-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8b1da-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="8b1da-107">Parent element</span></span>



| <span data-ttu-id="8b1da-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="8b1da-108">Element</span></span>                                                                              | <span data-ttu-id="8b1da-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="8b1da-109">Derived from</span></span>                                                           | <span data-ttu-id="8b1da-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8b1da-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="8b1da-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="8b1da-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="8b1da-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="8b1da-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="8b1da-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8b1da-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8b1da-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b1da-114">Remarks</span></span>

<span data-ttu-id="8b1da-115">Для разработки на C++ см. [**свойство From объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span><span class="sxs-lookup"><span data-stu-id="8b1da-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="8b1da-116">Сведения о разработке сценариев см. [**в разделе емаилактион. from**](emailaction-from.md).</span><span class="sxs-lookup"><span data-stu-id="8b1da-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1da-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8b1da-117">Requirements</span></span>



| <span data-ttu-id="8b1da-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8b1da-118">Requirement</span></span> | <span data-ttu-id="8b1da-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8b1da-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b1da-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b1da-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1da-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b1da-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8b1da-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b1da-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1da-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b1da-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





