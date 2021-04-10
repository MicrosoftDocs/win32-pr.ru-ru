---
title: Элемент title (Шовмессажетипе)
description: Содержит заголовок окна сообщения.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Элемент title планировщик задач
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135343"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="04f44-104">Элемент title (Шовмессажетипе)</span><span class="sxs-lookup"><span data-stu-id="04f44-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="04f44-105">Содержит заголовок окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="04f44-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="04f44-106">Элемент **Title** определяется сложным типом [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="04f44-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="04f44-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="04f44-107">Parent element</span></span>



| <span data-ttu-id="04f44-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="04f44-108">Element</span></span>                                                                                  | <span data-ttu-id="04f44-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="04f44-109">Derived from</span></span>                                                               | <span data-ttu-id="04f44-110">Описание</span><span class="sxs-lookup"><span data-stu-id="04f44-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="04f44-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="04f44-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="04f44-112">**шовмессажетипе**</span><span class="sxs-lookup"><span data-stu-id="04f44-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="04f44-113">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="04f44-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="04f44-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04f44-114">Remarks</span></span>

<span data-ttu-id="04f44-115">Сведения о разработке на языке C++ см. в разделе [**свойство Title объекта ишовмессажеактион**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span><span class="sxs-lookup"><span data-stu-id="04f44-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="04f44-116">Сведения о разработке сценариев см. в разделе [**шовмессажеактион. Title**](showmessageaction-title.md).</span><span class="sxs-lookup"><span data-stu-id="04f44-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04f44-117">Требования</span><span class="sxs-lookup"><span data-stu-id="04f44-117">Requirements</span></span>



| <span data-ttu-id="04f44-118">Требование</span><span class="sxs-lookup"><span data-stu-id="04f44-118">Requirement</span></span> | <span data-ttu-id="04f44-119">Значение</span><span class="sxs-lookup"><span data-stu-id="04f44-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04f44-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04f44-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04f44-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04f44-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04f44-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04f44-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04f44-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04f44-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





