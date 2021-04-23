---
title: Сложный тип Сендемаилтипе
description: Определяет тип действия, используемого для указания того, что при выполнении задачи будет отправлено сообщение электронной почты. Этот тип определяет все элементы, используемые для моделирования сообщения электронной почты.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- планировщик задач сложного типа Сендемаилтипе
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672900"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="61dad-105">Сложный тип Сендемаилтипе</span><span class="sxs-lookup"><span data-stu-id="61dad-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="61dad-106">Определяет тип действия, используемого для указания того, что при выполнении задачи будет отправлено сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="61dad-107">Этот тип определяет все элементы, используемые для моделирования сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="61dad-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="61dad-108">Child elements</span></span>



| <span data-ttu-id="61dad-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="61dad-109">Element</span></span>                                                                        | <span data-ttu-id="61dad-110">Тип</span><span class="sxs-lookup"><span data-stu-id="61dad-110">Type</span></span>                                                                         | <span data-ttu-id="61dad-111">Описание</span><span class="sxs-lookup"><span data-stu-id="61dad-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61dad-112">**Вложения**</span><span class="sxs-lookup"><span data-stu-id="61dad-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="61dad-113">**аттачментстипе**</span><span class="sxs-lookup"><span data-stu-id="61dad-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="61dad-114">Указывает список вложений в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="61dad-115">**Скрытая копия**</span><span class="sxs-lookup"><span data-stu-id="61dad-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="61dad-116">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-116">**string**</span></span>                                                                   | <span data-ttu-id="61dad-117">Указывает адреса электронной почты, используемые в строке СК сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="61dad-118">**Текст**</span><span class="sxs-lookup"><span data-stu-id="61dad-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="61dad-119">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-119">**string**</span></span>                                                                   | <span data-ttu-id="61dad-120">Задает текст в тексте сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="61dad-121">**Кому**</span><span class="sxs-lookup"><span data-stu-id="61dad-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="61dad-122">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-122">**string**</span></span>                                                                   | <span data-ttu-id="61dad-123">Указывает адреса электронной почты, используемые в строке CC сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="61dad-124">**Исходный тип**</span><span class="sxs-lookup"><span data-stu-id="61dad-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="61dad-125">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-125">**string**</span></span>                                                                   | <span data-ttu-id="61dad-126">Указывает адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="61dad-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="61dad-127">**хеадерфиелдс**</span><span class="sxs-lookup"><span data-stu-id="61dad-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="61dad-128">**хеадерфиелдстипе**</span><span class="sxs-lookup"><span data-stu-id="61dad-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="61dad-129">Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="61dad-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="61dad-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="61dad-131">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-131">**string**</span></span>                                                                   | <span data-ttu-id="61dad-132">Указывает адреса электронной почты, на которые вы ответили в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="61dad-133">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="61dad-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="61dad-134">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="61dad-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="61dad-135">Указывает сервер электронной почты, используемый для отправки сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="61dad-136">**Субъект**</span><span class="sxs-lookup"><span data-stu-id="61dad-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="61dad-137">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-137">**string**</span></span>                                                                   | <span data-ttu-id="61dad-138">Указывает тему сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="61dad-139">**Кому**</span><span class="sxs-lookup"><span data-stu-id="61dad-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="61dad-140">**string**</span><span class="sxs-lookup"><span data-stu-id="61dad-140">**string**</span></span>                                                                   | <span data-ttu-id="61dad-141">Указывает адреса электронной почты, на которые будет отправлено сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="61dad-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="61dad-142">Требования</span><span class="sxs-lookup"><span data-stu-id="61dad-142">Requirements</span></span>



| <span data-ttu-id="61dad-143">Требование</span><span class="sxs-lookup"><span data-stu-id="61dad-143">Requirement</span></span> | <span data-ttu-id="61dad-144">Значение</span><span class="sxs-lookup"><span data-stu-id="61dad-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61dad-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61dad-145">Minimum supported client</span></span><br/> | <span data-ttu-id="61dad-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61dad-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61dad-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61dad-147">Minimum supported server</span></span><br/> | <span data-ttu-id="61dad-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61dad-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





