---
title: Хеадерфиелд (Хеадерфиелдстипе), элемент
description: Содержит поле для заголовка в сообщении электронной почты.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- планировщик задач элемента Хеадерфиелд
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682135"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="df53c-104">Хеадерфиелд (Хеадерфиелдстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="df53c-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="df53c-105">Содержит поле для заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="df53c-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="df53c-106">Элемент **хеадерфиелд** определяется сложным типом [**хеадерфиелдстипе**](taskschedulerschema-headerfieldstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="df53c-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="df53c-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="df53c-107">Parent element</span></span>



| <span data-ttu-id="df53c-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="df53c-108">Element</span></span>                                                                        | <span data-ttu-id="df53c-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="df53c-109">Derived from</span></span>                                                                 | <span data-ttu-id="df53c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="df53c-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df53c-111">**хеадерфиелдс**</span><span class="sxs-lookup"><span data-stu-id="df53c-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="df53c-112">**хеадерфиелдстипе**</span><span class="sxs-lookup"><span data-stu-id="df53c-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="df53c-113">Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="df53c-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="df53c-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="df53c-114">Child elements</span></span>



| <span data-ttu-id="df53c-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="df53c-115">Element</span></span>                                                            | <span data-ttu-id="df53c-116">Тип</span><span class="sxs-lookup"><span data-stu-id="df53c-116">Type</span></span>                                                                    | <span data-ttu-id="df53c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="df53c-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="df53c-118">**Имя**</span><span class="sxs-lookup"><span data-stu-id="df53c-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="df53c-119">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="df53c-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="df53c-120">Задает имя поля заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="df53c-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="df53c-121">**Значение**</span><span class="sxs-lookup"><span data-stu-id="df53c-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="df53c-122">**string**</span><span class="sxs-lookup"><span data-stu-id="df53c-122">**string**</span></span>                                                              | <span data-ttu-id="df53c-123">Задает значение поля заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="df53c-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="df53c-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df53c-124">Remarks</span></span>

<span data-ttu-id="df53c-125">Сведения о разработке на языке C++ см. в разделе [**свойство хеадерфиелдс объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="df53c-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="df53c-126">Сведения о разработке сценариев см. в разделе [**емаилактион. хеадерфиелдс**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="df53c-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df53c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="df53c-127">Requirements</span></span>



| <span data-ttu-id="df53c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="df53c-128">Requirement</span></span> | <span data-ttu-id="df53c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="df53c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="df53c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df53c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="df53c-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df53c-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="df53c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df53c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="df53c-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df53c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





