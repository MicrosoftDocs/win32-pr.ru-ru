---
title: Свойство FontName (объект Commands)
description: Сведения о свойстве объекта FontName Commands. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068260"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="f2ba3-104">Свойство FontName (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="f2ba3-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="f2ba3-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f2ba3-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f2ba3-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f2ba3-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f2ba3-107">Возвращает или задает шрифт, используемый во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="f2ba3-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f2ba3-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f2ba3-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f2ba3-109">\*Символы Agent. \***("**_чарактерид_\*_"). Шрифт Commands. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="f2ba3-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="f2ba3-110">Часть</span><span class="sxs-lookup"><span data-stu-id="f2ba3-110">Part</span></span>   | <span data-ttu-id="f2ba3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f2ba3-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="f2ba3-112">*Шрифт*</span><span class="sxs-lookup"><span data-stu-id="f2ba3-112">*Font*</span></span> | <span data-ttu-id="f2ba3-113">Строковое значение, соответствующее имени шрифта.</span><span class="sxs-lookup"><span data-stu-id="f2ba3-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2ba3-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2ba3-114">Remarks</span></span>

<span data-ttu-id="f2ba3-115">Свойство **FontName** определяет шрифт, используемый для отображения текста во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="f2ba3-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="f2ba3-116">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или--если этот параметр не задан, используется пользовательский идентификатор языка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2ba3-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="f2ba3-117">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="f2ba3-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




