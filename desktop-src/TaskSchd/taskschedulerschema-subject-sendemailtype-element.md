---
title: Элемент subject (Сендемаилтипе)
description: Содержит тему сообщения электронной почты.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Элемент subject планировщик задач
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535489"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="8ae18-104">Элемент subject (Сендемаилтипе)</span><span class="sxs-lookup"><span data-stu-id="8ae18-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="8ae18-105">Содержит тему сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8ae18-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="8ae18-106">Элемент **subject** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae18-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8ae18-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="8ae18-107">Parent element</span></span>



| <span data-ttu-id="8ae18-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="8ae18-108">Element</span></span>                                                                              | <span data-ttu-id="8ae18-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="8ae18-109">Derived from</span></span>                                                           | <span data-ttu-id="8ae18-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8ae18-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="8ae18-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="8ae18-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="8ae18-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="8ae18-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="8ae18-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8ae18-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8ae18-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ae18-114">Remarks</span></span>

<span data-ttu-id="8ae18-115">Сведения о разработке на языке C++ см. в разделе [**свойство Subject объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span><span class="sxs-lookup"><span data-stu-id="8ae18-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="8ae18-116">Сведения о разработке сценариев см. в разделе [**емаилактион. subject**](emailaction-subject.md).</span><span class="sxs-lookup"><span data-stu-id="8ae18-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae18-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8ae18-117">Requirements</span></span>



| <span data-ttu-id="8ae18-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8ae18-118">Requirement</span></span> | <span data-ttu-id="8ae18-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8ae18-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ae18-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ae18-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae18-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ae18-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8ae18-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ae18-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae18-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8ae18-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





