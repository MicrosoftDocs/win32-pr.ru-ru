---
title: Сервер (Сендемаилтипе), элемент
description: Содержит почтовый сервер, используемый для отправки сообщения электронной почты.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Серверный элемент планировщик задач
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414972"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="d26df-104">Сервер (Сендемаилтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="d26df-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="d26df-105">Содержит почтовый сервер, используемый для отправки сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d26df-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="d26df-106">Элемент **Server** определяется сложным типом [**сендемаилтипе**](taskschedulerschema-sendemailtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d26df-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d26df-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="d26df-107">Parent element</span></span>



| <span data-ttu-id="d26df-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="d26df-108">Element</span></span>                                                                              | <span data-ttu-id="d26df-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="d26df-109">Derived from</span></span>                                                           | <span data-ttu-id="d26df-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d26df-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="d26df-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="d26df-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="d26df-112">**сендемаилтипе**</span><span class="sxs-lookup"><span data-stu-id="d26df-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="d26df-113">Представляет действие, которое отправляет сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d26df-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d26df-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d26df-114">Remarks</span></span>

<span data-ttu-id="d26df-115">Сведения о разработке на языке C++ см. в разделе [**свойство сервера иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span><span class="sxs-lookup"><span data-stu-id="d26df-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="d26df-116">Сведения о разработке сценариев см. в разделе [**емаилактион. Server**](emailaction-server.md).</span><span class="sxs-lookup"><span data-stu-id="d26df-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d26df-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d26df-117">Requirements</span></span>



| <span data-ttu-id="d26df-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d26df-118">Requirement</span></span> | <span data-ttu-id="d26df-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d26df-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d26df-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d26df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d26df-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d26df-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d26df-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d26df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d26df-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d26df-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





