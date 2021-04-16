---
title: Саундеффектс, свойство
description: Саундеффектс, свойство
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710065"
---
# <a name="soundeffects-property"></a><span data-ttu-id="42411-103">Саундеффектс, свойство</span><span class="sxs-lookup"><span data-stu-id="42411-103">SoundEffects Property</span></span>

<span data-ttu-id="42411-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="42411-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="42411-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="42411-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="42411-106">Возвращает логическое значение, указывающее, звучит ли звук (. WAV) файлы, настроенные как часть действий с символами, будут воспроизводиться.</span><span class="sxs-lookup"><span data-stu-id="42411-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="42411-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="42411-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="42411-108">*агент \* \* *. Аудиуутпут. Саундеффектс**</span><span class="sxs-lookup"><span data-stu-id="42411-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="42411-109">Значение</span><span class="sxs-lookup"><span data-stu-id="42411-109">Value</span></span>     | <span data-ttu-id="42411-110">Описание</span><span class="sxs-lookup"><span data-stu-id="42411-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="42411-111">**True**</span><span class="sxs-lookup"><span data-stu-id="42411-111">**True**</span></span>  | <span data-ttu-id="42411-112">Символьные звуковые эффекты включены.</span><span class="sxs-lookup"><span data-stu-id="42411-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="42411-113">**False**</span><span class="sxs-lookup"><span data-stu-id="42411-113">**False**</span></span> | <span data-ttu-id="42411-114">Символьные звуковые эффекты отключены.</span><span class="sxs-lookup"><span data-stu-id="42411-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42411-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42411-115">Remarks</span></span>

<span data-ttu-id="42411-116">Это свойство отражает параметр звуковые эффекты воспроизведения символа на странице вывод страницы свойств агента (дополнительные параметры символов).</span><span class="sxs-lookup"><span data-stu-id="42411-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="42411-117">Если свойство **саундеффектс** возвращает **значение true**, будут воспроизводиться звуковые эффекты, включенные в определение символа.</span><span class="sxs-lookup"><span data-stu-id="42411-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="42411-118">Если **значение равно false**, звуковые эффекты воспроизводиться не будут.</span><span class="sxs-lookup"><span data-stu-id="42411-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="42411-119">Параметр свойства влияет на все символы и доступен только для чтения; только пользователь может установить это значение свойства.</span><span class="sxs-lookup"><span data-stu-id="42411-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="42411-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="42411-120">See Also</span></span>

[<span data-ttu-id="42411-121">**Событие Ажентпропертичанже**</span><span class="sxs-lookup"><span data-stu-id="42411-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




