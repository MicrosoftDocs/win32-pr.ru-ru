---
title: Элемент Body (Сендемаилтипе)
description: Содержит текст в тексте сообщения электронной почты.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Элемент Body планировщик задач
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681948"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="80a99-104">Элемент Body (Сендемаилтипе)</span><span class="sxs-lookup"><span data-stu-id="80a99-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="80a99-105">Содержит текст в тексте сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="80a99-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="80a99-106">Элемент **Body** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="80a99-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="80a99-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="80a99-107">Parent element</span></span>



| <span data-ttu-id="80a99-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="80a99-108">Element</span></span>                                                                              | <span data-ttu-id="80a99-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="80a99-109">Derived from</span></span>                                                           | <span data-ttu-id="80a99-110">Описание</span><span class="sxs-lookup"><span data-stu-id="80a99-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="80a99-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="80a99-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="80a99-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="80a99-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="80a99-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="80a99-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="80a99-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80a99-114">Remarks</span></span>

<span data-ttu-id="80a99-115">Сведения о разработке на языке C++ см. в разделе [**свойство Body объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span><span class="sxs-lookup"><span data-stu-id="80a99-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="80a99-116">Сведения о разработке сценариев см. в разделе [**емаилактион. Body**](emailaction-body.md).</span><span class="sxs-lookup"><span data-stu-id="80a99-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80a99-117">Требования</span><span class="sxs-lookup"><span data-stu-id="80a99-117">Requirements</span></span>



| <span data-ttu-id="80a99-118">Требование</span><span class="sxs-lookup"><span data-stu-id="80a99-118">Requirement</span></span> | <span data-ttu-id="80a99-119">Значение</span><span class="sxs-lookup"><span data-stu-id="80a99-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80a99-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80a99-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80a99-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="80a99-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="80a99-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80a99-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80a99-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="80a99-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





