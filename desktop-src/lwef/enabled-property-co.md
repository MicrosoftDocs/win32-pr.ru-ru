---
title: Свойство Enabled (объект Command)
description: Сведения о свойстве объекта команды Enabled. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407337"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="cd249-104">Свойство Enabled (объект Command)</span><span class="sxs-lookup"><span data-stu-id="cd249-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="cd249-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cd249-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="cd249-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="cd249-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="cd249-107">Возвращает или задает значение, указывающее, включена ли **команда** во всплывающем меню указанного символа.</span><span class="sxs-lookup"><span data-stu-id="cd249-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="cd249-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="cd249-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="cd249-109">\*Агент \***. Символы ("**_чарактерид_*_"). Команды ("_*_имя_\*_"). Включено_ \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="cd249-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="cd249-110">Часть</span><span class="sxs-lookup"><span data-stu-id="cd249-110">Part</span></span>      | <span data-ttu-id="cd249-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cd249-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd249-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="cd249-112">*boolean*</span></span> | <span data-ttu-id="cd249-113">Логическое выражение, указывающее, включена ли **команда** .</span><span class="sxs-lookup"><span data-stu-id="cd249-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="cd249-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="cd249-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="cd249-115">**Команда** включена.</span><span class="sxs-lookup"><span data-stu-id="cd249-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="cd249-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**IsFalse**</dt></span><span class="sxs-lookup"><span data-stu-id="cd249-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="cd249-117">**Команда** отключена.</span><span class="sxs-lookup"><span data-stu-id="cd249-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd249-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="cd249-118">Remarks</span></span>

<span data-ttu-id="cd249-119">Если свойство [**Enabled**](enabled-property.md) имеет значение **true**, то в всплывающем меню символа заголовок объекта [**команды**](/windows/desktop/lwef/the-command-object) отображается как нормальный текст, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="cd249-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="cd249-120">Если свойство **Enabled** имеет **значение false**, заголовок отображается как недоступный (отключенный) текст.</span><span class="sxs-lookup"><span data-stu-id="cd249-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="cd249-121">Отключенная **команда** также недоступна для речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="cd249-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

