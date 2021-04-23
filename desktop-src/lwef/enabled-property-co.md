---
title: Свойство Enabled (объект Command)
description: Свойство Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691731"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="e9179-103">Свойство Enabled (объект Command)</span><span class="sxs-lookup"><span data-stu-id="e9179-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="e9179-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9179-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e9179-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="e9179-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e9179-106">Возвращает или задает значение, указывающее, включена ли **команда** во всплывающем меню указанного символа.</span><span class="sxs-lookup"><span data-stu-id="e9179-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="e9179-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e9179-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e9179-108">\*Агент \***. Символы ("**_чарактерид_*_"). Команды ("_*_имя_\*_"). Включено_ \*  \[  =  *логическое значение*\]</span><span class="sxs-lookup"><span data-stu-id="e9179-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="e9179-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="e9179-109">Part</span></span>      | <span data-ttu-id="e9179-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e9179-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9179-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="e9179-111">*boolean*</span></span> | <span data-ttu-id="e9179-112">Логическое выражение, указывающее, включена ли **команда** .</span><span class="sxs-lookup"><span data-stu-id="e9179-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="e9179-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="e9179-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="e9179-114">**Команда** включена.</span><span class="sxs-lookup"><span data-stu-id="e9179-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="e9179-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Неверно**</dt></span><span class="sxs-lookup"><span data-stu-id="e9179-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="e9179-116">**Команда** отключена.</span><span class="sxs-lookup"><span data-stu-id="e9179-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9179-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9179-117">Remarks</span></span>

<span data-ttu-id="e9179-118">Если свойство [**Enabled**](enabled-property.md) имеет значение **true**, то в всплывающем меню символа заголовок объекта [**команды**](/windows/desktop/lwef/the-command-object) отображается как нормальный текст, если клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="e9179-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="e9179-119">Если свойство **Enabled** имеет **значение false**, заголовок отображается как недоступный (отключенный) текст.</span><span class="sxs-lookup"><span data-stu-id="e9179-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="e9179-120">Отключенная **команда** также недоступна для речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="e9179-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

