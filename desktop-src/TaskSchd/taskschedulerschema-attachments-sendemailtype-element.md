---
title: Элемент вложений (Сендемаилтипе)
description: Содержит список вложений в сообщении электронной почты.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Элемент вложений планировщик задач
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803227"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="73c3e-104">Элемент вложений (Сендемаилтипе)</span><span class="sxs-lookup"><span data-stu-id="73c3e-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="73c3e-105">Содержит список вложений в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="73c3e-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="73c3e-106">Элемент **вложениям** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="73c3e-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="73c3e-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="73c3e-107">Parent element</span></span>



| <span data-ttu-id="73c3e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="73c3e-108">Element</span></span>                                                                              | <span data-ttu-id="73c3e-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="73c3e-109">Derived from</span></span>                                                           | <span data-ttu-id="73c3e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="73c3e-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="73c3e-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="73c3e-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="73c3e-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="73c3e-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="73c3e-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="73c3e-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="73c3e-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="73c3e-114">Child elements</span></span>



| <span data-ttu-id="73c3e-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="73c3e-115">Element</span></span>                                                          | <span data-ttu-id="73c3e-116">Тип</span><span class="sxs-lookup"><span data-stu-id="73c3e-116">Type</span></span>                                                                    | <span data-ttu-id="73c3e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="73c3e-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73c3e-118">**Файл**</span><span class="sxs-lookup"><span data-stu-id="73c3e-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="73c3e-119">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="73c3e-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="73c3e-120">Указывает путь к файлу, который отправляется в виде вложения в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="73c3e-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="73c3e-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73c3e-121">Remarks</span></span>

<span data-ttu-id="73c3e-122">Сведения о разработке на языке C++ см. в разделе [**свойство вложений иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="73c3e-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="73c3e-123">Сведения о разработке сценариев см. в разделе [**емаилактион. вложениям**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="73c3e-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73c3e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="73c3e-124">Requirements</span></span>



| <span data-ttu-id="73c3e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="73c3e-125">Requirement</span></span> | <span data-ttu-id="73c3e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="73c3e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="73c3e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73c3e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="73c3e-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73c3e-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="73c3e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73c3e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="73c3e-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="73c3e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





