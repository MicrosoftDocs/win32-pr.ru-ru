---
title: Свойство FontSize (объект Commands)
description: Сведения о свойстве объекта команд FontSize. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068211"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="e03d9-104">Свойство FontSize (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="e03d9-104">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="e03d9-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e03d9-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e03d9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="e03d9-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e03d9-107">Возвращает или задает размер шрифта, используемый во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="e03d9-107">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="e03d9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e03d9-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e03d9-109">\*Символы Agent. \***("**_чарактерид_\*_"). Команды. FontSize,_ \*  \[  =  *точки*\]</span><span class="sxs-lookup"><span data-stu-id="e03d9-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="e03d9-110">Часть</span><span class="sxs-lookup"><span data-stu-id="e03d9-110">Part</span></span>     | <span data-ttu-id="e03d9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e03d9-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="e03d9-112">*Точки*</span><span class="sxs-lookup"><span data-stu-id="e03d9-112">*Points*</span></span> | <span data-ttu-id="e03d9-113">Длинное целое значение, указывающее размер шрифта в пунктах.</span><span class="sxs-lookup"><span data-stu-id="e03d9-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e03d9-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="e03d9-114">Remarks</span></span>

<span data-ttu-id="e03d9-115">Свойство **FontSize** определяет размер шрифта, используемого для отображения текста во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="e03d9-115">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="e03d9-116">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или (если он не задан) — параметре языка пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e03d9-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="e03d9-117">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e03d9-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




