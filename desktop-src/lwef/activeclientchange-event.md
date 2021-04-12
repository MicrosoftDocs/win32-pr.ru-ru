---
title: Событие Активеклиентчанже
description: Событие Активеклиентчанже
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253268"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="3dae9-103">Событие Активеклиентчанже</span><span class="sxs-lookup"><span data-stu-id="3dae9-103">ActiveClientChange Event</span></span>

<span data-ttu-id="3dae9-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3dae9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3dae9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="3dae9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3dae9-106">Происходит при изменении активного клиента символа.</span><span class="sxs-lookup"><span data-stu-id="3dae9-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="3dae9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3dae9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3dae9-108">**Вспомогательный** *агент.* Активеклиентчанже (ByVal *чарактерид*, ByVal *Active* **)**</span><span class="sxs-lookup"><span data-stu-id="3dae9-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="3dae9-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="3dae9-109">Part</span></span>          | <span data-ttu-id="3dae9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3dae9-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dae9-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="3dae9-111">*CharacterID*</span></span> | <span data-ttu-id="3dae9-112">Возвращает идентификатор символа, для которого произошло событие.</span><span class="sxs-lookup"><span data-stu-id="3dae9-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="3dae9-113">*Активен*</span><span class="sxs-lookup"><span data-stu-id="3dae9-113">*Active*</span></span>      | <span data-ttu-id="3dae9-114">Логическое значение, указывающее, стал ли клиент активным или неактивным.</span><span class="sxs-lookup"><span data-stu-id="3dae9-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="3dae9-115">**Значение true** Клиентское приложение стало активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="3dae9-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="3dae9-116">**Значение false** Клиентское приложение больше не является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="3dae9-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3dae9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dae9-117">Remarks</span></span>

<span data-ttu-id="3dae9-118">Если несколько клиентских приложений совместно используют один и тот же символ, то активный клиент символа получает ввод с помощью мыши (например, элемент управления агента Microsoft Agent щелкнул или перетаскивает события).</span><span class="sxs-lookup"><span data-stu-id="3dae9-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="3dae9-119">Аналогично, когда отображается несколько символов, активный клиент самого верхнего символа (также известный как клиент ввода) получает события [команды](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="3dae9-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="3dae9-120">При изменении активного клиента символа это событие возвращает идентификатор этого символа и **значение true** , если приложение становится активным клиентом символа, или **значение false** , если оно больше не является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="3dae9-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="3dae9-121">Клиентское приложение может получить это событие, когда пользователь выбирает запись клиентского приложения во всплывающем меню символа или с помощью команды Voice, когда клиентское приложение изменяет состояние активности или когда другое клиентское приложение завершает соединение с агентом.</span><span class="sxs-lookup"><span data-stu-id="3dae9-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="3dae9-122">Агент отправляет это событие только в клиентские приложения, которые напрямую затрагиваются; либо Станьте активным клиентом, либо завершится активным клиентом.</span><span class="sxs-lookup"><span data-stu-id="3dae9-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="3dae9-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="3dae9-123">See Also</span></span>

<span data-ttu-id="3dae9-124">[\* \* \* \* Активатеинпут \* \* событие \* \*](activateinput-event.md), [\* \* \* \* активное \* \* свойство \* \*](active-property.md), [\* \* \* \* деактиватеинпут \* \* событие \* \*](deactivateinput-event.md), [\* \* \* \* Активация \* \* метод \* \*](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="3dae9-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





