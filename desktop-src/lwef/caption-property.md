---
title: Свойство Caption (объект Command)
description: Сведения о свойстве Caption объекта Command. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262556"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="f9230-104">Свойство Caption (объект Command)</span><span class="sxs-lookup"><span data-stu-id="f9230-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="f9230-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9230-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f9230-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f9230-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f9230-107">Определяет текст, отображаемый для [**команды**](/windows/desktop/lwef/the-command-object) во всплывающем меню указанного символа.</span><span class="sxs-lookup"><span data-stu-id="f9230-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f9230-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f9230-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f9230-109">\*Агент \***. Символы ("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Строка* заголовка\]</span><span class="sxs-lookup"><span data-stu-id="f9230-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="f9230-110">Часть</span><span class="sxs-lookup"><span data-stu-id="f9230-110">Part</span></span>     | <span data-ttu-id="f9230-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f9230-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9230-112">*строка*</span><span class="sxs-lookup"><span data-stu-id="f9230-112">*string*</span></span> | <span data-ttu-id="f9230-113">Строковое выражение, результатом которого является текст, отображаемый в качестве заголовка для **команды**.</span><span class="sxs-lookup"><span data-stu-id="f9230-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9230-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="f9230-114">Remarks</span></span>

<span data-ttu-id="f9230-115">Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.</span><span class="sxs-lookup"><span data-stu-id="f9230-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="f9230-116">Если вы не определили **воицекаптион** для команды, будет использоваться параметр **Caption** .</span><span class="sxs-lookup"><span data-stu-id="f9230-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
