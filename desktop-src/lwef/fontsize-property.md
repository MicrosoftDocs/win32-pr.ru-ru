---
title: Свойство FontSize (объект Commands)
description: Свойство FontSize
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84d5eb966dd7d0605bd0e4f17674fe4499bab6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105719187"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="9d27e-103">Свойство FontSize (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="9d27e-103">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="9d27e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9d27e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9d27e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9d27e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9d27e-106">Возвращает или задает размер шрифта, используемый во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="9d27e-106">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="9d27e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9d27e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9d27e-108">\*Символы Agent. \***("**_чарактерид_\*_"). Команды. FontSize,_ \*  \[  =  *точки*\]</span><span class="sxs-lookup"><span data-stu-id="9d27e-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="9d27e-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9d27e-109">Part</span></span>     | <span data-ttu-id="9d27e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9d27e-110">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="9d27e-111">*Точки*</span><span class="sxs-lookup"><span data-stu-id="9d27e-111">*Points*</span></span> | <span data-ttu-id="9d27e-112">Длинное целое значение, указывающее размер шрифта в пунктах.</span><span class="sxs-lookup"><span data-stu-id="9d27e-112">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d27e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d27e-113">Remarks</span></span>

<span data-ttu-id="9d27e-114">Свойство **FontSize** определяет размер шрифта, используемого для отображения текста во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="9d27e-114">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="9d27e-115">Значение по умолчанию для параметра Font основано на параметре шрифта меню для параметра **LanguageID** символа или (если он не задан) — параметре языка пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9d27e-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="9d27e-116">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="9d27e-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




