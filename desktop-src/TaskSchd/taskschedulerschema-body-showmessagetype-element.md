---
title: Элемент Body (Шовмессажетипе)
description: Содержит текст, отображаемый в тексте окна сообщения.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Элемент Body планировщик задач
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491361"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="a98ef-104">Элемент Body (Шовмессажетипе)</span><span class="sxs-lookup"><span data-stu-id="a98ef-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="a98ef-105">Содержит текст, отображаемый в тексте окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="a98ef-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="a98ef-106">Элемент **Body** определяется сложным типом [**шовмессажетипе**](taskschedulerschema-showmessagetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a98ef-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a98ef-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a98ef-107">Parent element</span></span>



| <span data-ttu-id="a98ef-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="a98ef-108">Element</span></span>                                                                                  | <span data-ttu-id="a98ef-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="a98ef-109">Derived from</span></span>                                                               | <span data-ttu-id="a98ef-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a98ef-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="a98ef-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="a98ef-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="a98ef-112">**шовмессажетипе**</span><span class="sxs-lookup"><span data-stu-id="a98ef-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="a98ef-113">Представляет действие, показывающее окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="a98ef-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a98ef-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a98ef-114">Remarks</span></span>

<span data-ttu-id="a98ef-115">Сведения о разработке на языке C++ см. в разделе [**свойство MessageBody объекта ишовмессажеактион**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span><span class="sxs-lookup"><span data-stu-id="a98ef-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="a98ef-116">Сведения о разработке сценариев см. в разделе [**шовмессажеактион. MessageBody**](showmessageaction-messagebody.md).</span><span class="sxs-lookup"><span data-stu-id="a98ef-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a98ef-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a98ef-117">Requirements</span></span>



| <span data-ttu-id="a98ef-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a98ef-118">Requirement</span></span> | <span data-ttu-id="a98ef-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a98ef-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a98ef-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a98ef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a98ef-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a98ef-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a98ef-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a98ef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a98ef-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a98ef-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





