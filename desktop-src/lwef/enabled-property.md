---
title: Свойство Enabled (объект всплывающего объекта)
description: Свойство Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691730"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="481d1-103">Свойство Enabled (объект всплывающего объекта)</span><span class="sxs-lookup"><span data-stu-id="481d1-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="481d1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="481d1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="481d1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="481d1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="481d1-106">Возвращает значение, указывающее, включено ли всплывающее сообщение для указанного символа.</span><span class="sxs-lookup"><span data-stu-id="481d1-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="481d1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="481d1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="481d1-108">\*Агент \***. Символы ("**_чарактерид_*_"). Всплывающее сообщение. включено_*</span><span class="sxs-lookup"><span data-stu-id="481d1-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="481d1-109">Значение</span><span class="sxs-lookup"><span data-stu-id="481d1-109">Value</span></span>     | <span data-ttu-id="481d1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="481d1-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="481d1-111">**True**</span><span class="sxs-lookup"><span data-stu-id="481d1-111">**True**</span></span>  | <span data-ttu-id="481d1-112">Всплывающее сообщение включено.</span><span class="sxs-lookup"><span data-stu-id="481d1-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="481d1-113">**False**</span><span class="sxs-lookup"><span data-stu-id="481d1-113">**False**</span></span> | <span data-ttu-id="481d1-114">Всплывающее сообщение отключено.</span><span class="sxs-lookup"><span data-stu-id="481d1-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="481d1-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="481d1-115">Remarks</span></span>

<span data-ttu-id="481d1-116">Свойство **Enabled** возвращает логическое значение, указывающее, включено ли всплывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="481d1-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="481d1-117">Состояние всплывающей подсказки по умолчанию задается как часть определения символа при компиляции символа в редакторе символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="481d1-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="481d1-118">Если символ определен так, что не поддерживает всплывающую подсказку, это свойство всегда будет иметь **значение false** для символа.</span><span class="sxs-lookup"><span data-stu-id="481d1-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




