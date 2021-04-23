---
title: Событие Ажентпропертичанже
description: Событие Ажентпропертичанже
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067756"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="07820-103">Событие Ажентпропертичанже</span><span class="sxs-lookup"><span data-stu-id="07820-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="07820-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07820-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="07820-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="07820-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="07820-106">Происходит, когда пользователь изменяет свойство в окне Дополнительные параметры символов.</span><span class="sxs-lookup"><span data-stu-id="07820-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="07820-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="07820-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="07820-108"> *Подагент.\ *\ *\ * ажентпропертичанже\**</span><span class="sxs-lookup"><span data-stu-id="07820-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="07820-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07820-109">Remarks</span></span>

<span data-ttu-id="07820-110">Это событие указывает, что пользователь изменил и применил все свойства, включенные в окно расширенного символа.</span><span class="sxs-lookup"><span data-stu-id="07820-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="07820-111">В коде, обрабатывающем это событие, можно запрашивать определенные настройки свойств объектов [аудиуутпут](the-audiooutput-object.md) или [спичинпут](the-speechinput-object.md) .</span><span class="sxs-lookup"><span data-stu-id="07820-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="07820-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="07820-112">See Also</span></span>

[<span data-ttu-id="07820-113">**Событие Дефаултчарактерчанже**</span><span class="sxs-lookup"><span data-stu-id="07820-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




