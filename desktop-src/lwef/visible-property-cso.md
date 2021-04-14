---
title: Свойство Visible (объект Commands)
description: Свойство Visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414613"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="c85b5-103">Свойство Visible (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="c85b5-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="c85b5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c85b5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c85b5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="c85b5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c85b5-106">Возвращает или задает значение, определяющее, отображается ли заголовок коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="c85b5-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="c85b5-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c85b5-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="c85b5-108">\*Агент \***. Символы (**"\* чарактерид \*" \* *). Команда. видимое* \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="c85b5-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="c85b5-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="c85b5-109">Part</span></span>      | <span data-ttu-id="c85b5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c85b5-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c85b5-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="c85b5-111">*boolean*</span></span> | <span data-ttu-id="c85b5-112">Логическое выражение, указывающее, отображается ли объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="c85b5-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="c85b5-113">**Значение true** Отобразится заголовок.</span><span class="sxs-lookup"><span data-stu-id="c85b5-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="c85b5-114">**Значение false** Заголовок не отображается.</span><span class="sxs-lookup"><span data-stu-id="c85b5-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c85b5-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c85b5-115">Remarks</span></span>

<span data-ttu-id="c85b5-116">Чтобы заголовок отображался во всплывающем меню символа, если приложение не является клиентом input-Active, для этого свойства необходимо задать значение **true** и свойство [**Caption**](caption-property.md) , заданное для коллекции команд.</span><span class="sxs-lookup"><span data-stu-id="c85b5-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="c85b5-117">Кроме того, для этого свойства необходимо задать значение **true** , чтобы команды в коллекции отображались во всплывающем меню, если приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="c85b5-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

