---
title: Элемент Task (Дефинитионтипе)
description: Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал. | Элемент Task (Дефинитионтипе)
ms.assetid: 0e880720-1896-43cf-b702-cabca8ab1430
keywords:
- Журнал событий элемента задачи
topic_type:
- apiref
api_name:
- task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 35fe629c17b8ede4064de3fb11d05c8e8c84f202
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693994"
---
# <a name="task-definitiontype-element"></a><span data-ttu-id="70206-105">Элемент Task (Дефинитионтипе)</span><span class="sxs-lookup"><span data-stu-id="70206-105">task (DefinitionType) Element</span></span>

<span data-ttu-id="70206-106">\[Начиная с компилятора сообщений, который поставляется с версией Windows SDK для Windows 7, этот элемент больше не доступен.\]</span><span class="sxs-lookup"><span data-stu-id="70206-106">\[Beginning with the message compiler that ships with the Windows 7 version of the Windows SDK, this element is no longer available.\]</span></span>

<span data-ttu-id="70206-107">Определяет событие, специфическое для задачи, которое поставщик может заносить в журнал.</span><span class="sxs-lookup"><span data-stu-id="70206-107">Defines a task-specific event that your provider can log.</span></span>

``` syntax
<xs:element name="task"
    type="TaskEventDefinitionType"
 />
```

<span data-ttu-id="70206-108">Элемент **Task** определяется сложным типом [**дефинитионтипе**](eventmanifestschema-definitiontype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="70206-108">The **task** element is defined by the [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="70206-109">Требования</span><span class="sxs-lookup"><span data-stu-id="70206-109">Requirements</span></span>



| <span data-ttu-id="70206-110">Требование</span><span class="sxs-lookup"><span data-stu-id="70206-110">Requirement</span></span> | <span data-ttu-id="70206-111">Значение</span><span class="sxs-lookup"><span data-stu-id="70206-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70206-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70206-112">Minimum supported client</span></span><br/> | <span data-ttu-id="70206-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70206-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70206-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70206-114">Minimum supported server</span></span><br/> | <span data-ttu-id="70206-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70206-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70206-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70206-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="70206-117">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="70206-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="70206-118">**события (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="70206-118">**events (ProviderType)**</span></span>](eventmanifestschema-events-providertype-element.md)
</dt> </dl>

 

 





