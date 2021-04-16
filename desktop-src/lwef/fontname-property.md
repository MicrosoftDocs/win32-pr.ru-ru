---
title: Свойство FontName (объект Commands)
description: FontName, свойство
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134966"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="9a7e5-103">Свойство FontName (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="9a7e5-103">FontName Property (Commands Object)</span></span>

<span data-ttu-id="9a7e5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a7e5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9a7e5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9a7e5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9a7e5-106">Возвращает или задает шрифт, используемый во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="9a7e5-106">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="9a7e5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9a7e5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9a7e5-108">\*Символы Agent. \***("**_чарактерид_\*_"). Шрифт Commands. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="9a7e5-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="9a7e5-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9a7e5-109">Part</span></span>   | <span data-ttu-id="9a7e5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9a7e5-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="9a7e5-111">*Шрифт*</span><span class="sxs-lookup"><span data-stu-id="9a7e5-111">*Font*</span></span> | <span data-ttu-id="9a7e5-112">Строковое значение, соответствующее имени шрифта.</span><span class="sxs-lookup"><span data-stu-id="9a7e5-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a7e5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a7e5-113">Remarks</span></span>

<span data-ttu-id="9a7e5-114">Свойство **FontName** определяет шрифт, используемый для отображения текста во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="9a7e5-114">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="9a7e5-115">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или--если этот параметр не задан, используется пользовательский идентификатор языка по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a7e5-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="9a7e5-116">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="9a7e5-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




