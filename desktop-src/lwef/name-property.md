---
title: Свойство Name (объект characters)
description: Сведения о свойстве Name объекта Characters. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989329"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="8134e-104">Свойство Name (объект characters)</span><span class="sxs-lookup"><span data-stu-id="8134e-104">Name Property (Characters Object)</span></span>

<span data-ttu-id="8134e-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8134e-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8134e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="8134e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8134e-107">Возвращает или задает строку, указывающую имя по умолчанию указанного символа.</span><span class="sxs-lookup"><span data-stu-id="8134e-107">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="8134e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="8134e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8134e-109">\*Агент \***. Символы ("**_чарактерид_\*_")._ \*  \[  =  *Строка* имени\]</span><span class="sxs-lookup"><span data-stu-id="8134e-109">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="8134e-110">Часть</span><span class="sxs-lookup"><span data-stu-id="8134e-110">Part</span></span>     | <span data-ttu-id="8134e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8134e-111">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8134e-112">*строка*</span><span class="sxs-lookup"><span data-stu-id="8134e-112">*string*</span></span> | <span data-ttu-id="8134e-113">Строковое значение, соответствующее имени символа (в текущем параметре языка).</span><span class="sxs-lookup"><span data-stu-id="8134e-113">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8134e-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="8134e-114">Remarks</span></span>

<span data-ttu-id="8134e-115">**Имя** символа может зависеть от параметра [**LanguageID**](languageid-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="8134e-115">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="8134e-116">Имя символа на одном языке может отличаться или использовать другие символы, чем в другом.</span><span class="sxs-lookup"><span data-stu-id="8134e-116">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="8134e-117">**Имя** символа по умолчанию для конкретного языка определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8134e-117">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="8134e-118">Избегайте переименования символа, особенно при его использовании в сценарии, где другие клиентские приложения могут использовать один и тот же символ.</span><span class="sxs-lookup"><span data-stu-id="8134e-118">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="8134e-119">Кроме того, агент использует **имя** символа для автоматического создания команд для скрытия и отображения символа.</span><span class="sxs-lookup"><span data-stu-id="8134e-119">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




