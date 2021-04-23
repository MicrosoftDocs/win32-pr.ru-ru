---
title: Хеадерфиелдс (Сендемаилтипе), элемент
description: Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- планировщик задач элемента Хеадерфиелдс
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534577"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="cb255-104">Хеадерфиелдс (Сендемаилтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="cb255-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="cb255-105">Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cb255-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="cb255-106">Элемент **хеадерфиелдс** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cb255-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cb255-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cb255-107">Parent element</span></span>



| <span data-ttu-id="cb255-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cb255-108">Element</span></span>                                                                              | <span data-ttu-id="cb255-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="cb255-109">Derived from</span></span>                                                           | <span data-ttu-id="cb255-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cb255-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="cb255-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="cb255-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="cb255-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="cb255-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="cb255-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cb255-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="cb255-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cb255-114">Child elements</span></span>



| <span data-ttu-id="cb255-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="cb255-115">Element</span></span>                                                                         | <span data-ttu-id="cb255-116">Тип</span><span class="sxs-lookup"><span data-stu-id="cb255-116">Type</span></span>                                                                       | <span data-ttu-id="cb255-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cb255-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="cb255-118">**хеадерфиелд**</span><span class="sxs-lookup"><span data-stu-id="cb255-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="cb255-119">**хеадерфиелдтипе**</span><span class="sxs-lookup"><span data-stu-id="cb255-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="cb255-120">Содержит поле для заголовка в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cb255-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="cb255-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb255-121">Remarks</span></span>

<span data-ttu-id="cb255-122">Сведения о разработке на языке C++ см. в разделе [**свойство хеадерфиелдс объекта иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span><span class="sxs-lookup"><span data-stu-id="cb255-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="cb255-123">Сведения о разработке сценариев см. в разделе [**емаилактион. хеадерфиелдс**](emailaction-headerfields.md).</span><span class="sxs-lookup"><span data-stu-id="cb255-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb255-124">Требования</span><span class="sxs-lookup"><span data-stu-id="cb255-124">Requirements</span></span>



| <span data-ttu-id="cb255-125">Требование</span><span class="sxs-lookup"><span data-stu-id="cb255-125">Requirement</span></span> | <span data-ttu-id="cb255-126">Значение</span><span class="sxs-lookup"><span data-stu-id="cb255-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb255-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb255-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cb255-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb255-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb255-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb255-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cb255-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb255-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





