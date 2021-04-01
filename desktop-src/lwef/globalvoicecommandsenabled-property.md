---
title: Глобалвоицекоммандсенаблед, свойство
description: Глобалвоицекоммандсенаблед, свойство
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987520"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="c72ba-103">Глобалвоицекоммандсенаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="c72ba-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="c72ba-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c72ba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c72ba-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="c72ba-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c72ba-106">Возвращает или задает значение, указывающее, включена ли поддержка голоса для глобальных команд агента.</span><span class="sxs-lookup"><span data-stu-id="c72ba-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="c72ba-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c72ba-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c72ba-108">*Субагент. ***Символы ("*** чарактерид \* \* *"). Commands. Глобалвоицекоммандсенаблед**</span><span class="sxs-lookup"><span data-stu-id="c72ba-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="c72ba-109">\[ = *логическая*\]</span><span class="sxs-lookup"><span data-stu-id="c72ba-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="c72ba-110">Отделение</span><span class="sxs-lookup"><span data-stu-id="c72ba-110">Part</span></span>      | <span data-ttu-id="c72ba-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c72ba-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c72ba-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="c72ba-112">*boolean*</span></span> | <span data-ttu-id="c72ba-113">Логическое выражение, указывающее, включены ли параметры голоса для глобальных команд агента.</span><span class="sxs-lookup"><span data-stu-id="c72ba-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="c72ba-114">**True** (по умолчанию) параметры голоса включены.</span><span class="sxs-lookup"><span data-stu-id="c72ba-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="c72ba-115">**Значение false** Параметры голоса отключены.</span><span class="sxs-lookup"><span data-stu-id="c72ba-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c72ba-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c72ba-116">Remarks</span></span>

<span data-ttu-id="c72ba-117">Microsoft Agent автоматически добавляет параметры голоса (грамматики) для открытия и закрытия окна "Voice Commands", а также для отображения и скрытия символа.</span><span class="sxs-lookup"><span data-stu-id="c72ba-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="c72ba-118">Если для **глобалвоицекоммандсенаблед** задано **значение false**, то агент отключает любые параметры голоса для этих команд, а также параметры голоса для [**заголовка**](caption-property.md) объектов [**команд**](/windows/desktop/lwef/the-commands-collection-object) других клиентов.</span><span class="sxs-lookup"><span data-stu-id="c72ba-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="c72ba-119">Это позволяет исключить их из текущей активной грамматики клиента.</span><span class="sxs-lookup"><span data-stu-id="c72ba-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="c72ba-120">Однако, так как это потенциально блокирует голосовой доступ к другим клиентам, сбросьте это свойство в **значение true** после обработки речевого ввода пользователя.</span><span class="sxs-lookup"><span data-stu-id="c72ba-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="c72ba-121">Отключение свойства не влияет на всплывающее меню символа.</span><span class="sxs-lookup"><span data-stu-id="c72ba-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="c72ba-122">Глобальные команды, добавленные сервером, по-прежнему будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="c72ba-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="c72ba-123">Их нельзя удалить из всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="c72ba-123">You cannot remove them from the pop-up menu.</span></span>

 

