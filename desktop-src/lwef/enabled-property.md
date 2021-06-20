---
title: Свойство Enabled (объект всплывающего объекта)
description: Сведения о включенном свойстве всплывающего объекта. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407307"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="3e55f-104">Свойство Enabled (объект всплывающего объекта)</span><span class="sxs-lookup"><span data-stu-id="3e55f-104">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="3e55f-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3e55f-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3e55f-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="3e55f-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3e55f-107">Возвращает значение, указывающее, включено ли всплывающее сообщение для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="3e55f-107">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="3e55f-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="3e55f-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3e55f-109">\*Агент \***. Символы ("**_чарактерид_*_"). Всплывающее сообщение. включено_*</span><span class="sxs-lookup"><span data-stu-id="3e55f-109">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="3e55f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="3e55f-110">Value</span></span>     | <span data-ttu-id="3e55f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3e55f-111">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="3e55f-112">**True**</span><span class="sxs-lookup"><span data-stu-id="3e55f-112">**True**</span></span>  | <span data-ttu-id="3e55f-113">Всплывающее сообщение включено.</span><span class="sxs-lookup"><span data-stu-id="3e55f-113">The balloon is enabled.</span></span>  |
| <span data-ttu-id="3e55f-114">**False**</span><span class="sxs-lookup"><span data-stu-id="3e55f-114">**False**</span></span> | <span data-ttu-id="3e55f-115">Всплывающее сообщение отключено.</span><span class="sxs-lookup"><span data-stu-id="3e55f-115">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e55f-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="3e55f-116">Remarks</span></span>

<span data-ttu-id="3e55f-117">Свойство **Enabled** возвращает логическое значение, указывающее, включено ли всплывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="3e55f-117">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="3e55f-118">Состояние всплывающей подсказки по умолчанию задается как часть определения символа при компиляции символа в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3e55f-118">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3e55f-119">Если символ определен так, что не поддерживает всплывающую подсказку, это свойство всегда будет иметь **значение false** для символа.</span><span class="sxs-lookup"><span data-stu-id="3e55f-119">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




