---
title: Свойство Description (устаревшие функции среды Windows)
description: Свойство Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070956"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="05d55-103">Свойство Description (устаревшие функции среды Windows)</span><span class="sxs-lookup"><span data-stu-id="05d55-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="05d55-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05d55-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="05d55-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="05d55-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="05d55-106">Возвращает или задает строку, указывающую описание указанного символа.</span><span class="sxs-lookup"><span data-stu-id="05d55-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="05d55-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="05d55-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="05d55-108">*Агент*. **Символы ("**_чарактерид_*_")._* \[  =  *Строка* описания\]</span><span class="sxs-lookup"><span data-stu-id="05d55-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="05d55-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="05d55-109">Part</span></span>     | <span data-ttu-id="05d55-110">Описание</span><span class="sxs-lookup"><span data-stu-id="05d55-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d55-111">*string*</span><span class="sxs-lookup"><span data-stu-id="05d55-111">*string*</span></span> | <span data-ttu-id="05d55-112">Строковое значение, соответствующее описанию символа (в текущем параметре языка).</span><span class="sxs-lookup"><span data-stu-id="05d55-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05d55-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05d55-113">Remarks</span></span>

<span data-ttu-id="05d55-114">**Описание** символа может зависеть от параметра **LanguageID** символа.</span><span class="sxs-lookup"><span data-stu-id="05d55-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="05d55-115">Имя символа на одном языке может отличаться или использовать другие символы, чем в другом.</span><span class="sxs-lookup"><span data-stu-id="05d55-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="05d55-116">**Описание** символа по умолчанию для конкретного языка определяется при компиляции символа с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="05d55-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="05d55-117">Параметр свойства **Description** является необязательным и не может быть указан для всех символов.</span><span class="sxs-lookup"><span data-stu-id="05d55-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




