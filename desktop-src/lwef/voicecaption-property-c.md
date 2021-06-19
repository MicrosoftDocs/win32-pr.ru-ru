---
title: Свойство Воицекаптион (объект Command)
description: Сведения о свойстве Воицекаптион объекта Command, который задает или возвращает текст, отображаемый для командного объекта в окне "Voice Commands".
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396169"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="f2018-103">Свойство Воицекаптион (объект Command)</span><span class="sxs-lookup"><span data-stu-id="f2018-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="f2018-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f2018-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f2018-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="f2018-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f2018-106">Задает или возвращает текст, отображаемый для [**командного**](/windows/desktop/lwef/the-command-object) объекта в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="f2018-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="f2018-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="f2018-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f2018-108">\*Символы Agent. \***("**_чарактерид_*_"). Команды ("_*_имя_\*_")._ \*  \[  =  *Строка* воицекаптион\]</span><span class="sxs-lookup"><span data-stu-id="f2018-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="f2018-109">Часть</span><span class="sxs-lookup"><span data-stu-id="f2018-109">Part</span></span>     | <span data-ttu-id="f2018-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f2018-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="f2018-111">*строка*</span><span class="sxs-lookup"><span data-stu-id="f2018-111">*string*</span></span> | <span data-ttu-id="f2018-112">Строковое выражение, результатом которого является отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="f2018-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2018-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2018-113">Remarks</span></span>

<span data-ttu-id="f2018-114">Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](https://www.bing.com/search?q=**Commands**) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="f2018-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="f2018-115">Этот текст будет отображаться в окне "Voice Commands", если ваше клиентское приложение является активным, а сам символ является видимым.</span><span class="sxs-lookup"><span data-stu-id="f2018-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="f2018-116">Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="f2018-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="f2018-117">Если не задано ни одно свойство **воицекаптион** и **Caption** , команда не отображается в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="f2018-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="f2018-118">См. также</span><span class="sxs-lookup"><span data-stu-id="f2018-118">See Also</span></span>

[<span data-ttu-id="f2018-119">**Свойство Caption**</span><span class="sxs-lookup"><span data-stu-id="f2018-119">**Caption property**</span></span>](caption-property.md)


 

 
