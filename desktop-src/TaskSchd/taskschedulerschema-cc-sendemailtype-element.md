---
title: Элемент CC (Сендемаилтипе)
description: Содержит адреса электронной почты, используемые в строке CC сообщения электронной почты.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- планировщик задач элемента CC
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491685"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="e41a4-104">Элемент CC (Сендемаилтипе)</span><span class="sxs-lookup"><span data-stu-id="e41a4-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="e41a4-105">Содержит адреса электронной почты, используемые в строке CC сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e41a4-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="e41a4-106">Элемент **CC** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e41a4-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e41a4-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e41a4-107">Parent element</span></span>



| <span data-ttu-id="e41a4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e41a4-108">Element</span></span>                                                                              | <span data-ttu-id="e41a4-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="e41a4-109">Derived from</span></span>                                                           | <span data-ttu-id="e41a4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e41a4-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="e41a4-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="e41a4-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="e41a4-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="e41a4-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="e41a4-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e41a4-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e41a4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e41a4-114">Remarks</span></span>

<span data-ttu-id="e41a4-115">Сведения о разработке C++ см. в разделе [**свойство CC объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span><span class="sxs-lookup"><span data-stu-id="e41a4-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="e41a4-116">Сведения о разработке сценариев см. в разделе [**EmailAction.CC**](emailaction-cc.md).</span><span class="sxs-lookup"><span data-stu-id="e41a4-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e41a4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e41a4-117">Requirements</span></span>



| <span data-ttu-id="e41a4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e41a4-118">Requirement</span></span> | <span data-ttu-id="e41a4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e41a4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e41a4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e41a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e41a4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e41a4-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e41a4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e41a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e41a4-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e41a4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





