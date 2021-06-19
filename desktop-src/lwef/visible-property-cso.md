---
title: Свойство Visible (объект Commands)
description: Сведения о свойстве Visible объекта Commands, который определяет, отображается ли заголовок коллекции команд во всплывающем меню символа.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ea780ed5f19dbe732b18de741f9d7ee376df67
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396259"
---
# <a name="visible-property-commands-object"></a><span data-ttu-id="1c9aa-103">Свойство Visible (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="1c9aa-103">Visible Property (Commands Object)</span></span>

<span data-ttu-id="1c9aa-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1c9aa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1c9aa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="1c9aa-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1c9aa-106">Возвращает или задает значение, определяющее, отображается ли заголовок коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="1c9aa-106">Returns or sets a value that determines whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection's caption appears in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="1c9aa-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="1c9aa-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="1c9aa-108">\*Агент \***. Символы (**"\* чарактерид \*" \* *). Команда. видимое* \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="1c9aa-108">*agent\***.Characters(**"* CharacterID *"\*\*).Commands.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="1c9aa-109">Часть</span><span class="sxs-lookup"><span data-stu-id="1c9aa-109">Part</span></span>      | <span data-ttu-id="1c9aa-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1c9aa-110">Description</span></span>                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9aa-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="1c9aa-111">*boolean*</span></span> | <span data-ttu-id="1c9aa-112">Логическое выражение, указывающее, отображается ли объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="1c9aa-112">A Boolean expression specifying whether your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object appears in the character's pop-up menu.</span></span> <br/> <span data-ttu-id="1c9aa-113">**Значение true** Отобразится заголовок.</span><span class="sxs-lookup"><span data-stu-id="1c9aa-113">**True** The caption appears.</span></span><br/> <span data-ttu-id="1c9aa-114">**Значение false** Заголовок не отображается.</span><span class="sxs-lookup"><span data-stu-id="1c9aa-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c9aa-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="1c9aa-115">Remarks</span></span>

<span data-ttu-id="1c9aa-116">Чтобы заголовок отображался во всплывающем меню символа, если приложение не является клиентом input-Active, для этого свойства необходимо задать значение **true** и свойство [**Caption**](caption-property.md) , заданное для коллекции команд.</span><span class="sxs-lookup"><span data-stu-id="1c9aa-116">For the caption to appear in the character's pop-up menu when your application is not the input-active client, this property must be set to **True** and the [**Caption**](caption-property.md) property set for your Commands collection.</span></span> <span data-ttu-id="1c9aa-117">Кроме того, для этого свойства необходимо задать значение **true** , чтобы команды в коллекции отображались во всплывающем меню, если приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="1c9aa-117">In addition, this property must be set to **True** for commands in your collection to appear in the pop-up menu when your application is input-active.</span></span>

 

