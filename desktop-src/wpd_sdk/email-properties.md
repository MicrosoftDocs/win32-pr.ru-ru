---
description: Портативные устройства Windows поддерживают следующие свойства электронной почты.
ms.assetid: c886622e-57e7-4bd1-b645-0e979ee7b66a
title: Свойства электронной почты (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Email
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: de25d73e9fb331538ecdbf5f22306d85c282b338
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675700"
---
# <a name="email-properties"></a><span data-ttu-id="9f7ad-103">Свойства электронной почты</span><span class="sxs-lookup"><span data-stu-id="9f7ad-103">Email Properties</span></span>

<span data-ttu-id="9f7ad-104">Портативные устройства Windows поддерживают следующие свойства электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-104">Windows Portable Devices supports the following email properties.</span></span>



| <span data-ttu-id="9f7ad-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="9f7ad-105">Property</span></span>                         | <span data-ttu-id="9f7ad-106">VarType</span><span class="sxs-lookup"><span data-stu-id="9f7ad-106">VarType</span></span>        | <span data-ttu-id="9f7ad-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9f7ad-107">Description</span></span>                                                                                                                               |
|----------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7ad-108">**\_ \_ строка скрытия сообщения электронной почты WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-108">**WPD\_EMAIL\_BCC\_LINE**</span></span>        | <span data-ttu-id="9f7ad-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9f7ad-110">Получатели скрытой копии сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-110">The BCC recipients of the e-mail message.</span></span> <span data-ttu-id="9f7ad-111">Получатели СКРЫТой копии получают копию сообщения, но их имена не отображаются как получатели.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-111">BCC recipients receive a copy of the e-mail, but their names are not displayed as recipients.</span></span>   |
| <span data-ttu-id="9f7ad-112">**\_Электронная почта WPD — \_ \_ строка CC**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-112">**WPD\_EMAIL\_CC\_LINE**</span></span>         | <span data-ttu-id="9f7ad-113">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-113">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9f7ad-114">Получатели копии сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-114">The CC recipients of the e-mail message.</span></span> <span data-ttu-id="9f7ad-115">Получатели копии получают копию сообщения электронной почты, и их имена отображаются как получатели.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-115">CC recipients receive a copy of the e-mail message, and their names are displayed as recipients.</span></span> |
| <span data-ttu-id="9f7ad-116">**\_сообщения электронной почты WPD \_ с \_ вложениями**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-116">**WPD\_EMAIL\_HAS\_ATTACHMENTS**</span></span> | <span data-ttu-id="9f7ad-117">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-117">**VT\_BOOL**</span></span>   | <span data-ttu-id="9f7ad-118">Логическое значение, указывающее, есть ли у этого сообщения электронной почты вложения.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-118">A Boolean value that specifies whether this e-mail message has attachments.</span></span>                                                               |
| <span data-ttu-id="9f7ad-119">**\_Прочитано электронное письмо WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-119">**WPD\_EMAIL\_HAS\_BEEN\_READ**</span></span>  | <span data-ttu-id="9f7ad-120">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-120">**VT\_BOOL**</span></span>   | <span data-ttu-id="9f7ad-121">Логическое значение, указывающее, было ли Прочитано это сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-121">A Boolean value that specifies whether this e-mail message has been read.</span></span>                                                                 |
| <span data-ttu-id="9f7ad-122">**\_время получения электронной почты WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-122">**WPD\_EMAIL\_RECEIVED\_TIME**</span></span>   | <span data-ttu-id="9f7ad-123">**\_Дата VT**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-123">**VT\_DATE**</span></span>   | <span data-ttu-id="9f7ad-124">Значение, указывающее, когда было получено сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-124">A value that specifies when the e-mail message was received.</span></span>                                                                              |
| <span data-ttu-id="9f7ad-125">**\_ \_ адрес отправителя электронной почты WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-125">**WPD\_EMAIL\_SENDER\_ADDRESS**</span></span>  | <span data-ttu-id="9f7ad-126">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-126">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9f7ad-127">Адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-127">The e-mail address of the sender.</span></span>                                                                                                         |
| <span data-ttu-id="9f7ad-128">**\_сообщение электронной почты WPD \_ по \_ строке**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-128">**WPD\_EMAIL\_TO\_LINE**</span></span>         | <span data-ttu-id="9f7ad-129">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="9f7ad-130">Основные получатели сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9f7ad-130">The main recipients of the e-mail message.</span></span>                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="9f7ad-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9f7ad-131">Requirements</span></span>



| <span data-ttu-id="9f7ad-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9f7ad-132">Requirement</span></span> | <span data-ttu-id="9f7ad-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9f7ad-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f7ad-134">Header</span><span class="sxs-lookup"><span data-stu-id="9f7ad-134">Header</span></span><br/> | <dl> <span data-ttu-id="9f7ad-135"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f7ad-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f7ad-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f7ad-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f7ad-137">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="9f7ad-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




