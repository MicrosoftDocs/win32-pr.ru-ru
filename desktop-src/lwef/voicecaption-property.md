---
title: Свойство Воицекаптион (объект Commands)
description: Воицекаптион, свойство
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800760"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="b3760-103">Свойство Воицекаптион (объект Commands)</span><span class="sxs-lookup"><span data-stu-id="b3760-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="b3760-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3760-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b3760-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="b3760-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b3760-106">Возвращает или задает текст, отображаемый для объекта [**Commands**](/windows/desktop/lwef/the-commands-collection-object) в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="b3760-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="b3760-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b3760-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b3760-108">\*Символы Agent. \***("**_чарактерид_\*_"). Строка Commands. воицекаптион_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="b3760-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="b3760-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="b3760-109">Part</span></span>     | <span data-ttu-id="b3760-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b3760-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="b3760-111">*string*</span><span class="sxs-lookup"><span data-stu-id="b3760-111">*string*</span></span> | <span data-ttu-id="b3760-112">Строковое выражение, результатом которого является отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="b3760-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3760-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3760-113">Remarks</span></span>

<span data-ttu-id="b3760-114">Если задать свойство [**Voice**](voice-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , то обычно также устанавливается свойство **воицекаптион** .</span><span class="sxs-lookup"><span data-stu-id="b3760-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="b3760-115">Параметр текст **воицекаптион** отображается в окне "Voice Commands", если клиентское приложение является входным, а сам символ является видимым.</span><span class="sxs-lookup"><span data-stu-id="b3760-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="b3760-116">Если это свойство не задано, то отображаемый текст определяется параметром свойства [**Caption**](caption-property.md) коллекции **Commands** .</span><span class="sxs-lookup"><span data-stu-id="b3760-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="b3760-117">Если ни одно свойство **воицекаптион** или **Caption** не задано, команды в коллекции отображаются в окне "командные строки" в разделе "(неопределенная команда)", когда клиентское приложение становится входным.</span><span class="sxs-lookup"><span data-stu-id="b3760-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="b3760-118">Параметр **воицекаптион** также определяет текст, отображаемый в Tip прослушивания для указания команд, прослушиваемых этим символом.</span><span class="sxs-lookup"><span data-stu-id="b3760-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3760-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="b3760-119">See Also</span></span>

[<span data-ttu-id="b3760-120">Свойство Caption</span><span class="sxs-lookup"><span data-stu-id="b3760-120">Caption property</span></span>](caption-property.md)


 

 
