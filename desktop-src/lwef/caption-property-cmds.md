---
title: Свойство Caption (объект коллекции Commands)
description: Свойство Caption
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010fe051568f71c4940b4bcf964f257ba9f52ca
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134922"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="c27d3-103">Свойство Caption (объект коллекции Commands)</span><span class="sxs-lookup"><span data-stu-id="c27d3-103">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="c27d3-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c27d3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c27d3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="c27d3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c27d3-106">Определяет текст, отображаемый для объекта [**Command**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="c27d3-106">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="c27d3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c27d3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c27d3-108">\*Агент \***. Символы ("**_чарактерид_\*_")._ \* [Строка Commands. Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="c27d3-108">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="c27d3-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="c27d3-109">Part</span></span>     | <span data-ttu-id="c27d3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c27d3-110">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="c27d3-111">*string*</span><span class="sxs-lookup"><span data-stu-id="c27d3-111">*string*</span></span> | <span data-ttu-id="c27d3-112">Строковое выражение, результатом которого является текст, отображаемый в качестве заголовка.</span><span class="sxs-lookup"><span data-stu-id="c27d3-112">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c27d3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c27d3-113">Remarks</span></span>

<span data-ttu-id="c27d3-114">Установка свойства [**Caption**](caption-property.md) для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение true, а приложение не является клиентом ввода-активного.</span><span class="sxs-lookup"><span data-stu-id="c27d3-114">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="c27d3-115">Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.</span><span class="sxs-lookup"><span data-stu-id="c27d3-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="c27d3-116">При определении команд для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , имеющей [**заголовок**](caption-property.md), обычно также определяется **заголовок** для связанной с ней **команды** .</span><span class="sxs-lookup"><span data-stu-id="c27d3-116">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
