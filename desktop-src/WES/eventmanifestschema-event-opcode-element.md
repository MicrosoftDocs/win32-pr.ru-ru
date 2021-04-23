---
title: Элемент Event (код операции)
description: Определяет событие для кода операции, относящейся к конкретной задаче.
ms.assetid: 7ca8fff2-ef1a-45c4-b082-e4745330bf0b
keywords:
- Журнал событий элемента события
topic_type:
- apiref
api_name:
- event
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25f7a7f3a92c07895529d6dad59df22a7389735d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691961"
---
# <a name="event-opcode-element"></a><span data-ttu-id="ba5c2-104">Элемент Event (код операции)</span><span class="sxs-lookup"><span data-stu-id="ba5c2-104">event (opcode) Element</span></span>

<span data-ttu-id="ba5c2-105">\[Начиная с компилятора сообщений, который поставляется с версией Windows SDK для Windows 7, этот элемент больше не доступен.\]</span><span class="sxs-lookup"><span data-stu-id="ba5c2-105">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="ba5c2-106">Определяет событие для кода операции, относящейся к конкретной задаче.</span><span class="sxs-lookup"><span data-stu-id="ba5c2-106">Defines an event for a task-specific opcode.</span></span>

``` syntax
<xs:element name="event"
    type="EventDefinitionType"
 />
```

<span data-ttu-id="ba5c2-107">Элемент **event** определяется элементом [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ba5c2-107">The **event** element is defined by the [**opcode**](eventmanifestschema-opcode-taskeventdefinitiontype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5c2-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ba5c2-108">Requirements</span></span>



| <span data-ttu-id="ba5c2-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ba5c2-109">Requirement</span></span> | <span data-ttu-id="ba5c2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ba5c2-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba5c2-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba5c2-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5c2-112">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba5c2-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba5c2-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba5c2-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5c2-114">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba5c2-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba5c2-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba5c2-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba5c2-116">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="ba5c2-116">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ba5c2-117">**код операции (Таскевентдефинитионтипе)**</span><span class="sxs-lookup"><span data-stu-id="ba5c2-117">**opcode (TaskEventDefinitionType)**</span></span>](eventmanifestschema-opcode-taskeventdefinitiontype-element.md)
</dt> </dl>

 

 





