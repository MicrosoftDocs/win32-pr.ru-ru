---
title: Элемент File (Аттачментстипе)
description: Содержит путь к файлу, отправленному в виде вложения в сообщение электронной почты.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- планировщик задач элемента File
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415237"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="63507-104">Элемент File (Аттачментстипе)</span><span class="sxs-lookup"><span data-stu-id="63507-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="63507-105">Содержит путь к файлу, отправленному в виде вложения в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="63507-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="63507-106">Элемент **File** определяется сложным типом [**аттачментстипе**](taskschedulerschema-attachmentstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="63507-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="63507-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="63507-107">Parent element</span></span>



| <span data-ttu-id="63507-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="63507-108">Element</span></span>                                                                                      | <span data-ttu-id="63507-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="63507-109">Derived from</span></span>                                                               | <span data-ttu-id="63507-110">Описание</span><span class="sxs-lookup"><span data-stu-id="63507-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="63507-111">**Вложения (Сендемаилтипе)**</span><span class="sxs-lookup"><span data-stu-id="63507-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="63507-112">**аттачментстипе**</span><span class="sxs-lookup"><span data-stu-id="63507-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="63507-113">Содержит список вложений в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="63507-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="63507-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63507-114">Remarks</span></span>

<span data-ttu-id="63507-115">Сведения о разработке на языке C++ см. в разделе [**свойство вложений иемаилактион**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="63507-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="63507-116">Сведения о разработке сценариев см. в разделе [**емаилактион. вложениям**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="63507-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="63507-117">Требования</span><span class="sxs-lookup"><span data-stu-id="63507-117">Requirements</span></span>



| <span data-ttu-id="63507-118">Требование</span><span class="sxs-lookup"><span data-stu-id="63507-118">Requirement</span></span> | <span data-ttu-id="63507-119">Значение</span><span class="sxs-lookup"><span data-stu-id="63507-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63507-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63507-120">Minimum supported client</span></span><br/> | <span data-ttu-id="63507-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63507-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63507-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63507-122">Minimum supported server</span></span><br/> | <span data-ttu-id="63507-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63507-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





