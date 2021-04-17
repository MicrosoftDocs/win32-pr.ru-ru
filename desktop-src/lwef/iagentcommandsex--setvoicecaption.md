---
title: Иаженткоммандсекс Сетвоицекаптион
description: Иаженткоммандсекс Сетвоицекаптион
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710276"
---
# <a name="iagentcommandsexsetvoicecaption"></a><span data-ttu-id="a4e5d-103">Иаженткоммандсекс:: Сетвоицекаптион</span><span class="sxs-lookup"><span data-stu-id="a4e5d-103">IAgentCommandsEx::SetVoiceCaption</span></span>

<span data-ttu-id="a4e5d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4e5d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="a4e5d-105">Задает текст [**воицекаптион**](voicecaption-property.md) , отображаемый для [**командного**](/windows/desktop/lwef/the-command-object) объекта.</span><span class="sxs-lookup"><span data-stu-id="a4e5d-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="a4e5d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a4e5d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a4e5d-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*бсзвоицекаптион*</span><span class="sxs-lookup"><span data-stu-id="a4e5d-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="a4e5d-108">Значение типа BSTR, указывающее текст для свойства [**воицекаптион**](voicecaption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="a4e5d-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="a4e5d-109">Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e5d-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="a4e5d-110">Этот текст будет отображаться в окне "Voice Commands", если ваше клиентское приложение является активным, а сам символ является видимым.</span><span class="sxs-lookup"><span data-stu-id="a4e5d-110">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="a4e5d-111">Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="a4e5d-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="a4e5d-112">Если ни одно свойство **воицекаптион** или **Caption** не задано, команда не отображается в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="a4e5d-112">When neither the **VoiceCaption** or **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4e5d-113">См. также:</span><span class="sxs-lookup"><span data-stu-id="a4e5d-113">See Also</span></span>

[<span data-ttu-id="a4e5d-114">**Иаженткоммандсекс:: Жетвоицекаптион**</span><span class="sxs-lookup"><span data-stu-id="a4e5d-114">**IAgentCommandsEx::GetVoiceCaption**</span></span>](iagentcommandsex--getvoicecaption.md)


 

 