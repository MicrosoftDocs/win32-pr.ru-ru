---
title: Сложный тип Регистратионинфотипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Регистратионинфо.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- планировщик задач сложного типа Регистратионинфотипе
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988948"
---
# <a name="registrationinfotype-complex-type"></a><span data-ttu-id="fe44d-104">Сложный тип Регистратионинфотипе</span><span class="sxs-lookup"><span data-stu-id="fe44d-104">registrationInfoType Complex Type</span></span>

<span data-ttu-id="fe44d-105">Определяет дочерние элементы и сведения о последовательности для элемента [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fe44d-105">Defines the child elements and sequencing information for the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fe44d-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fe44d-106">Child elements</span></span>



| <span data-ttu-id="fe44d-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="fe44d-107">Element</span></span>                                                                                           | <span data-ttu-id="fe44d-108">Тип</span><span class="sxs-lookup"><span data-stu-id="fe44d-108">Type</span></span>     | <span data-ttu-id="fe44d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fe44d-109">Description</span></span>                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe44d-110">**Автор**</span><span class="sxs-lookup"><span data-stu-id="fe44d-110">**Author**</span></span>](taskschedulerschema-author-registrationinfotype-element.md)                         | <span data-ttu-id="fe44d-111">строка</span><span class="sxs-lookup"><span data-stu-id="fe44d-111">string</span></span>   | <span data-ttu-id="fe44d-112">Указывает автора задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-112">Specifies the author of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="fe44d-113">**Дата**</span><span class="sxs-lookup"><span data-stu-id="fe44d-113">**Date**</span></span>](taskschedulerschema-date-registrationinfotype-element.md)                             | <span data-ttu-id="fe44d-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="fe44d-114">dateTime</span></span> | <span data-ttu-id="fe44d-115">Указывает дату и время регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-115">Specifies the date and time when the task is registered.</span></span><br/>                                                |
| [<span data-ttu-id="fe44d-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe44d-116">**Description**</span></span>](taskschedulerschema-description-registrationinfotype-element.md)               | <span data-ttu-id="fe44d-117">строка</span><span class="sxs-lookup"><span data-stu-id="fe44d-117">string</span></span>   | <span data-ttu-id="fe44d-118">Указание описания задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-118">Specifies the description of the task.</span></span><br/>                                                                  |
| [<span data-ttu-id="fe44d-119">**Документация**</span><span class="sxs-lookup"><span data-stu-id="fe44d-119">**Documentation**</span></span>](taskschedulerschema-documentation-registrationinfotype-element.md)           | <span data-ttu-id="fe44d-120">строка</span><span class="sxs-lookup"><span data-stu-id="fe44d-120">string</span></span>   | <span data-ttu-id="fe44d-121">Указывает любую дополнительную документацию для задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-121">Specifies any additional documentation for the task.</span></span><br/>                                                    |
| [<span data-ttu-id="fe44d-122">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fe44d-122">**SecurityDescriptor**</span></span>](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | <span data-ttu-id="fe44d-123">строка</span><span class="sxs-lookup"><span data-stu-id="fe44d-123">string</span></span>   | <span data-ttu-id="fe44d-124">Указывает дескриптор безопасности задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-124">Specifies the security descriptor of the task.</span></span><br/>                                                          |
| [<span data-ttu-id="fe44d-125">**Источника**</span><span class="sxs-lookup"><span data-stu-id="fe44d-125">**Source**</span></span>](taskschedulerschema-source-registrationinfotype-element.md)                         | <span data-ttu-id="fe44d-126">строка</span><span class="sxs-lookup"><span data-stu-id="fe44d-126">string</span></span>   | <span data-ttu-id="fe44d-127">Указывает, откуда поступила задача.</span><span class="sxs-lookup"><span data-stu-id="fe44d-127">Specifies where the task originated from.</span></span> <span data-ttu-id="fe44d-128">Например, из компонента, службы, приложения или пользователя.</span><span class="sxs-lookup"><span data-stu-id="fe44d-128">For example, from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="fe44d-129">**URI**</span><span class="sxs-lookup"><span data-stu-id="fe44d-129">**URI**</span></span>](taskschedulerschema-uri-registrationinfotype-element.md)                               | <span data-ttu-id="fe44d-130">anyURI</span><span class="sxs-lookup"><span data-stu-id="fe44d-130">anyURI</span></span>   | <span data-ttu-id="fe44d-131">Указывает универсальный код ресурса (URI) задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-131">Specifies the URI of the task.</span></span><br/>                                                                          |
| [<span data-ttu-id="fe44d-132">**Версия**</span><span class="sxs-lookup"><span data-stu-id="fe44d-132">**Version**</span></span>](taskschedulerschema-version-registrationinfotype-element.md)                       | <span data-ttu-id="fe44d-133">строка</span><span class="sxs-lookup"><span data-stu-id="fe44d-133">string</span></span>   | <span data-ttu-id="fe44d-134">Указывает номер версии задачи.</span><span class="sxs-lookup"><span data-stu-id="fe44d-134">Specifies the version number of the task.</span></span><br/>                                                               |



## <a name="requirements"></a><span data-ttu-id="fe44d-135">Требования</span><span class="sxs-lookup"><span data-stu-id="fe44d-135">Requirements</span></span>



| <span data-ttu-id="fe44d-136">Требование</span><span class="sxs-lookup"><span data-stu-id="fe44d-136">Requirement</span></span> | <span data-ttu-id="fe44d-137">Значение</span><span class="sxs-lookup"><span data-stu-id="fe44d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe44d-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe44d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="fe44d-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe44d-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe44d-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe44d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="fe44d-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe44d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe44d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe44d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe44d-143">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="fe44d-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="fe44d-144">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fe44d-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





