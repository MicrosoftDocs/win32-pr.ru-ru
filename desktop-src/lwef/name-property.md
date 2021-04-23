---
title: Свойство Name (объект characters)
description: Свойство Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488730"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="4c562-103">Свойство Name (объект characters)</span><span class="sxs-lookup"><span data-stu-id="4c562-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="4c562-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4c562-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4c562-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="4c562-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4c562-106">Возвращает или задает строку, указывающую имя по умолчанию указанного символа.</span><span class="sxs-lookup"><span data-stu-id="4c562-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="4c562-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="4c562-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4c562-108">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[  =  *Строка* имени\]</span><span class="sxs-lookup"><span data-stu-id="4c562-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="4c562-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="4c562-109">Part</span></span>     | <span data-ttu-id="4c562-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4c562-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c562-111">*string*</span><span class="sxs-lookup"><span data-stu-id="4c562-111">*string*</span></span> | <span data-ttu-id="4c562-112">Строковое значение, соответствующее имени символа (в текущем параметре языка).</span><span class="sxs-lookup"><span data-stu-id="4c562-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c562-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c562-113">Remarks</span></span>

<span data-ttu-id="4c562-114">**Имя** символа может зависеть от параметра [**LanguageID**](languageid-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="4c562-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="4c562-115">Имя символа на одном языке может отличаться или использовать другие символы, чем в другом.</span><span class="sxs-lookup"><span data-stu-id="4c562-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="4c562-116">**Имя** символа по умолчанию для конкретного языка определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4c562-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="4c562-117">Избегайте переименования символа, особенно при его использовании в сценарии, где другие клиентские приложения могут использовать один и тот же символ.</span><span class="sxs-lookup"><span data-stu-id="4c562-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="4c562-118">Кроме того, агент использует **имя** символа для автоматического создания команд для скрытия и отображения символа.</span><span class="sxs-lookup"><span data-stu-id="4c562-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




