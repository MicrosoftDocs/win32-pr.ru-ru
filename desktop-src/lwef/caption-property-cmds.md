---
title: Свойство Caption (объект коллекции Commands)
description: Сведения о свойстве Caption объекта коллекции команд. Microsoft Agent является устаревшим в Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262056"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="f92d1-104">Свойство Caption (объект коллекции Commands)</span><span class="sxs-lookup"><span data-stu-id="f92d1-104">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="f92d1-105">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f92d1-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f92d1-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f92d1-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f92d1-107">Определяет текст, отображаемый для объекта [**Command**](/windows/desktop/lwef/the-commands-collection-object) во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="f92d1-107">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f92d1-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f92d1-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f92d1-109">\*Агент \***. Символы ("**_чарактерид_\*_")._ \* [Строка Commands. Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="f92d1-109">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="f92d1-110">Часть</span><span class="sxs-lookup"><span data-stu-id="f92d1-110">Part</span></span>     | <span data-ttu-id="f92d1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f92d1-111">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="f92d1-112">*строка*</span><span class="sxs-lookup"><span data-stu-id="f92d1-112">*string*</span></span> | <span data-ttu-id="f92d1-113">Строковое выражение, результатом которого является текст, отображаемый в качестве заголовка.</span><span class="sxs-lookup"><span data-stu-id="f92d1-113">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f92d1-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="f92d1-114">Remarks</span></span>

<span data-ttu-id="f92d1-115">Установка свойства [**Caption**](caption-property.md) для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение true, а приложение не является клиентом ввода-активного.</span><span class="sxs-lookup"><span data-stu-id="f92d1-115">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="f92d1-116">Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.</span><span class="sxs-lookup"><span data-stu-id="f92d1-116">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="f92d1-117">При определении команд для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , имеющей [**заголовок**](caption-property.md), обычно также определяется **заголовок** для связанной с ней **команды** .</span><span class="sxs-lookup"><span data-stu-id="f92d1-117">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
