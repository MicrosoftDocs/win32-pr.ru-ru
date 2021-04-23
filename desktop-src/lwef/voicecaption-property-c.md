---
title: Свойство Воицекаптион (объект Command)
description: Воицекаптион, свойство
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710426"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="7c098-103">Свойство Воицекаптион (объект Command)</span><span class="sxs-lookup"><span data-stu-id="7c098-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="7c098-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7c098-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="7c098-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="7c098-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="7c098-106">Задает или возвращает текст, отображаемый для [**командного**](/windows/desktop/lwef/the-command-object) объекта в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="7c098-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="7c098-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="7c098-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="7c098-108">\*Символы Agent. \***("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Строка* воицекаптион\]</span><span class="sxs-lookup"><span data-stu-id="7c098-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="7c098-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="7c098-109">Part</span></span>     | <span data-ttu-id="7c098-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7c098-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="7c098-111">*string*</span><span class="sxs-lookup"><span data-stu-id="7c098-111">*string*</span></span> | <span data-ttu-id="7c098-112">Строковое выражение, результатом которого является отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="7c098-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c098-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c098-113">Remarks</span></span>

<span data-ttu-id="7c098-114">Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](https://www.bing.com/search?q=**Commands**) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7c098-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="7c098-115">Этот текст будет отображаться в окне "Voice Commands", если ваше клиентское приложение является активным, а сам символ является видимым.</span><span class="sxs-lookup"><span data-stu-id="7c098-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="7c098-116">Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="7c098-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="7c098-117">Если не задано ни одно свойство **воицекаптион** и **Caption** , команда не отображается в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="7c098-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="7c098-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="7c098-118">See Also</span></span>

[<span data-ttu-id="7c098-119">**Свойство Caption**</span><span class="sxs-lookup"><span data-stu-id="7c098-119">**Caption property**</span></span>](caption-property.md)


 

 
