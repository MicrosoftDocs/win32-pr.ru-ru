---
title: Элемент BCC (Сендемаилтипе)
description: Содержит адреса электронной почты, используемые в строке СК сообщения электронной почты.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Элемент скрытой планировщик задач
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136346"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="68cdc-104">Элемент BCC (Сендемаилтипе)</span><span class="sxs-lookup"><span data-stu-id="68cdc-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="68cdc-105">Содержит адреса электронной почты, используемые в строке СК сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="68cdc-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="68cdc-106">Элемент **BCC** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="68cdc-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="68cdc-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="68cdc-107">Parent element</span></span>



| <span data-ttu-id="68cdc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="68cdc-108">Element</span></span>                                                                              | <span data-ttu-id="68cdc-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="68cdc-109">Derived from</span></span>                                                           | <span data-ttu-id="68cdc-110">Описание</span><span class="sxs-lookup"><span data-stu-id="68cdc-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="68cdc-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="68cdc-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="68cdc-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="68cdc-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="68cdc-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="68cdc-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="68cdc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68cdc-114">Remarks</span></span>

<span data-ttu-id="68cdc-115">Сведения о разработке на языке C++ см. в разделе [**свойство BCC объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span><span class="sxs-lookup"><span data-stu-id="68cdc-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="68cdc-116">Сведения о разработке сценариев см. в разделе [**емаилактион. BCC**](emailaction-bcc.md).</span><span class="sxs-lookup"><span data-stu-id="68cdc-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68cdc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="68cdc-117">Requirements</span></span>



| <span data-ttu-id="68cdc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="68cdc-118">Requirement</span></span> | <span data-ttu-id="68cdc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="68cdc-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="68cdc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68cdc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68cdc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68cdc-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="68cdc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68cdc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68cdc-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68cdc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





