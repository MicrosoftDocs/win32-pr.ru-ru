---
title: Свойство Visible (объект Command)
description: Свойство Visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710411"
---
# <a name="visible-property-command-object"></a><span data-ttu-id="fa25c-103">Свойство Visible (объект Command)</span><span class="sxs-lookup"><span data-stu-id="fa25c-103">Visible Property (Command Object)</span></span>

<span data-ttu-id="fa25c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa25c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fa25c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="fa25c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fa25c-106">Возвращает или задает значение, указывающее, отображается ли [**команда**](/windows/desktop/lwef/the-command-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="fa25c-106">Returns or sets whether the [**Command**](/windows/desktop/lwef/the-command-object) is visible in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="fa25c-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="fa25c-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="fa25c-108">\*Агент \***. Символы (**"\* чарактерид *"**). Команды (**"* имя \*" \* *). Видимое* \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="fa25c-108">*agent\***.Characters(**"* CharacterID *"**).Commands(**"* name *"\*\*).Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="fa25c-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="fa25c-109">Part</span></span>      | <span data-ttu-id="fa25c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fa25c-110">Description</span></span>                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa25c-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="fa25c-111">*boolean*</span></span> | <span data-ttu-id="fa25c-112">Логическое выражение, указывающее, отображается ли заголовок [**команды**](/windows/desktop/lwef/the-command-object)во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="fa25c-112">A Boolean expression specifying whether the [**Command**](/windows/desktop/lwef/the-command-object)'s caption appears in the character's pop-up menu.</span></span><br/> <span data-ttu-id="fa25c-113">**True** (по умолчанию) заголовок отображается.</span><span class="sxs-lookup"><span data-stu-id="fa25c-113">**True** (Default) The caption appears.</span></span><br/> <span data-ttu-id="fa25c-114">**Значение false** Заголовок не отображается.</span><span class="sxs-lookup"><span data-stu-id="fa25c-114">**False** The caption does not appear.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa25c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa25c-115">Remarks</span></span>

<span data-ttu-id="fa25c-116">Присвойте этому свойству **значение false** , если вы хотите включить речевой ввод для собственных интерфейсов, не выполняя их во всплывающем меню для символа.</span><span class="sxs-lookup"><span data-stu-id="fa25c-116">Set this property to **False** when you want to include voice input for your own interfaces without having them appear in the pop-up menu for the character.</span></span> <span data-ttu-id="fa25c-117">Если задать для свойства [**Caption**](caption-property.md) объекта [**команды**](/windows/desktop/lwef/the-command-object) пустую строку (""), текст заголовка не будет отображаться во всплывающем меню (например, в виде пустой строки), независимо от значения свойства [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fa25c-117">If you set a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md) property to the empty string (""), the caption text will not appear in the pop-up menu (for example, as a blank line), regardless of its [**Visible**](visible-property.md) property setting.</span></span>

<span data-ttu-id="fa25c-118">Значение свойства [**Visible**](visible-property.md) коллекции родительских [**команд**](/windows/desktop/lwef/the-commands-collection-object) объекта [**команды**](/windows/desktop/lwef/the-command-object) не влияет на значение свойства **Visible** **команды**.</span><span class="sxs-lookup"><span data-stu-id="fa25c-118">The [**Visible**](visible-property.md) property setting of a [**Command**](/windows/desktop/lwef/the-command-object) object's parent [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection does not affect the **Visible** property setting of the **Command**.</span></span>

 

