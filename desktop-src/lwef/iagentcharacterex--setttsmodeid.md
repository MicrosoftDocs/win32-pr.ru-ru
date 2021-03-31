---
title: Иажентчарактерекс Сетттсмодеид
description: Иажентчарактерекс Сетттсмодеид
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412619"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="e70f0-103">Иажентчарактерекс:: Сетттсмодеид</span><span class="sxs-lookup"><span data-stu-id="e70f0-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="e70f0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e70f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="e70f0-105">Задает идентификатор режима для модуля TTS, установленного для символа.</span><span class="sxs-lookup"><span data-stu-id="e70f0-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="e70f0-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e70f0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e70f0-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*бсзмодеид*</span><span class="sxs-lookup"><span data-stu-id="e70f0-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="e70f0-108">Параметр ID режима модуля TTS для символа.</span><span class="sxs-lookup"><span data-stu-id="e70f0-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="e70f0-109">**Иажентчарактерекс: сетттсмодеид** может завершиться ошибкой, если не установлен Speech.dll и указанный модуль не соответствует параметру режима TTS, скомпилированному для символа.</span><span class="sxs-lookup"><span data-stu-id="e70f0-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="e70f0-110">Этот параметр определяет предпочтительный режим обработчика для вывода речевого текста символа.</span><span class="sxs-lookup"><span data-stu-id="e70f0-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="e70f0-111">Идентификатор режима для подсистемы TTS (преобразование текста в речь) — это идентификатор GUID, определяемый поставщиком речи, который однозначно определяет режим подсистемы (отформатированный с помощью фигурных скобок и дефисов).</span><span class="sxs-lookup"><span data-stu-id="e70f0-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="e70f0-112">Дополнительные сведения см. в [документации по Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="e70f0-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="e70f0-113">Если задать идентификатор режима TTS, он переопределит попытку сервера сопоставить речевой механизм, основываясь на ИДЕНТИФИКАТОРе режима TTS, текущем коде языка системы и текущем ИДЕНТИФИКАТОРе языка символа.</span><span class="sxs-lookup"><span data-stu-id="e70f0-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="e70f0-114">Однако при попытке задать идентификатор режима, если пользователь отключил речевой вывод на странице свойств Microsoft Agent или если соответствующий обработчик не установлен, вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="e70f0-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="e70f0-115">Если для символа не задан идентификатор режима модуля TTS, сервер устанавливает подсистему, соответствующую языковому параметру символа (с помощью интерфейсов API распознавания речи Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="e70f0-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="e70f0-116">Задание этого свойства приведет к загрузке связанного обработчика, если он еще не загружен.</span><span class="sxs-lookup"><span data-stu-id="e70f0-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="e70f0-117">Это свойство применяется только к используемому в клиентском приложении символу. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e70f0-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="e70f0-118">Требования к речевому подсистему агента Microsoft Agent основаны на Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="e70f0-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="e70f0-119">Модули, поддерживающие требования к SAPI Microsoft Agent, можно установить и использовать с агентом.</span><span class="sxs-lookup"><span data-stu-id="e70f0-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="e70f0-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="e70f0-120">See Also</span></span>

[<span data-ttu-id="e70f0-121">**Иажентчарактерекс: Жетттсмодеид**</span><span class="sxs-lookup"><span data-stu-id="e70f0-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




