---
title: Свойство Caption (объект Command)
description: Свойство Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710419"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="705f4-103">Свойство Caption (объект Command)</span><span class="sxs-lookup"><span data-stu-id="705f4-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="705f4-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="705f4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="705f4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="705f4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="705f4-106">Определяет текст, отображаемый для [**команды**](/windows/desktop/lwef/the-command-object) во всплывающем меню указанного символа.</span><span class="sxs-lookup"><span data-stu-id="705f4-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="705f4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="705f4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="705f4-108">\*Агент \***. Символы ("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Строка* заголовка\]</span><span class="sxs-lookup"><span data-stu-id="705f4-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="705f4-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="705f4-109">Part</span></span>     | <span data-ttu-id="705f4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="705f4-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="705f4-111">*string*</span><span class="sxs-lookup"><span data-stu-id="705f4-111">*string*</span></span> | <span data-ttu-id="705f4-112">Строковое выражение, результатом которого является текст, отображаемый в качестве заголовка для **команды**.</span><span class="sxs-lookup"><span data-stu-id="705f4-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="705f4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="705f4-113">Remarks</span></span>

<span data-ttu-id="705f4-114">Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.</span><span class="sxs-lookup"><span data-stu-id="705f4-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="705f4-115">Если вы не определили **воицекаптион** для команды, будет использоваться параметр **Caption** .</span><span class="sxs-lookup"><span data-stu-id="705f4-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
