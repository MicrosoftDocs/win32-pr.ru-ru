---
title: Срмодеид, свойство
description: Срмодеид, свойство
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700705"
---
# <a name="srmodeid-property"></a><span data-ttu-id="53632-103">Срмодеид, свойство</span><span class="sxs-lookup"><span data-stu-id="53632-103">SRModeID Property</span></span>

<span data-ttu-id="53632-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53632-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="53632-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="53632-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="53632-106">Возвращает или задает модуль распознавания речи, используемый символом.</span><span class="sxs-lookup"><span data-stu-id="53632-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="53632-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="53632-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="53632-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Срмодеид* \*  \[  =  *модеид*\]</span><span class="sxs-lookup"><span data-stu-id="53632-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="53632-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="53632-109">Part</span></span>     | <span data-ttu-id="53632-110">Описание</span><span class="sxs-lookup"><span data-stu-id="53632-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="53632-111">*модеид*</span><span class="sxs-lookup"><span data-stu-id="53632-111">*ModeID*</span></span> | <span data-ttu-id="53632-112">Строковое выражение, соответствующее ИДЕНТИФИКАТОРу режима обработчика речи.</span><span class="sxs-lookup"><span data-stu-id="53632-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53632-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53632-113">Remarks</span></span>

<span data-ttu-id="53632-114">Свойство определяет подсистему распознавания речи, используемую символом для речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="53632-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="53632-115">Идентификатор режима для модуля распознавания речи — это отформатированная строка, определяемая поставщиком речи, которая уникально идентифицирует подсистему.</span><span class="sxs-lookup"><span data-stu-id="53632-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="53632-116">Дополнительные сведения см. [в разделе доступ к модулю распознавания речи в коде](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="53632-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="53632-117">Если указать идентификатор режима для обработчика речи, который не установлен, то, если пользователь отключил распознавание речи (на странице свойств Microsoft Agent) или если язык указанного обработчика речи не соответствует параметру [**LanguageID**](languageid-property.md) символа, сервер выдает ошибку.</span><span class="sxs-lookup"><span data-stu-id="53632-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="53632-118">Если вы запрашиваете это свойство и не установили (успешно) установку модуля распознавания речи, сервер возвращает идентификатор режима ядра, возвращаемого SAPI, на основе параметра [**LanguageID**](languageid-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="53632-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="53632-119">Если вы не задали **LanguageID** символа, агент возвращает идентификатор режима ядра, возвращаемого SAPI, на основе параметра идентификатора языка по умолчанию для пользователя.</span><span class="sxs-lookup"><span data-stu-id="53632-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="53632-120">Если соответствующий механизм отсутствует, сервер возвращает пустую строку ("").</span><span class="sxs-lookup"><span data-stu-id="53632-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="53632-121">Для запроса этого свойства не требуется, чтобы свойство [**спичинпут. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) было установлено в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="53632-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="53632-122">Однако если вы запрашиваете свойство, когда речевой ввод отключен, сервер возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="53632-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="53632-123">Если речевой ввод включен (в окне Дополнительные параметры символов), при запросе или задании этого свойства будет загружен соответствующий обработчик (если он еще не загружен) и запущены службы речи.</span><span class="sxs-lookup"><span data-stu-id="53632-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="53632-124">Это значит, что ключ прослушивания доступен и подсказка прослушивания доступна для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="53632-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="53632-125">(Ключ прослушивания и TIP прослушивания включены, только если они также включены в дополнительных параметрах символов.) Однако если вы запрашиваете свойство, когда речь отключена, сервер не запускает речевые службы.</span><span class="sxs-lookup"><span data-stu-id="53632-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="53632-126">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="53632-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="53632-127">Требования к речевому подсистему агента Microsoft Agent основаны на Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="53632-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="53632-128">Модули, поддерживающие требования к SAPI Microsoft Agent, можно установить и использовать с агентом.</span><span class="sxs-lookup"><span data-stu-id="53632-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="53632-129">Это свойство также возвращает пустую строку, если в системе не установлена совместимая поддержка звука.</span><span class="sxs-lookup"><span data-stu-id="53632-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="53632-130">Запрос этого свойства обычно не возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="53632-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="53632-131">Тем не менее, если при загрузке обработчика речи занимает слишком много времени, может возникнуть ошибка, указывающая, что время ожидания запроса истекло.</span><span class="sxs-lookup"><span data-stu-id="53632-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="53632-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="53632-132">See Also</span></span>

[<span data-ttu-id="53632-133">**LanguageID, свойство**</span><span class="sxs-lookup"><span data-stu-id="53632-133">**LanguageID property**</span></span>](languageid-property.md)


 

 




