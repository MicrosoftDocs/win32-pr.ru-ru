---
title: Ттсмодеид, свойство
description: Ттсмодеид, свойство
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258878"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="6e191-103">Ттсмодеид, свойство</span><span class="sxs-lookup"><span data-stu-id="6e191-103">TTSModeID Property</span></span>

<span data-ttu-id="6e191-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6e191-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6e191-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="6e191-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6e191-106">Возвращает или задает режим модуля TTS, используемый для символа.</span><span class="sxs-lookup"><span data-stu-id="6e191-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="6e191-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="6e191-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6e191-108">\*Агент ***. Символы ("*** чарактерид \* \* *"). Ттсмодеид* \*  \[  =  *модеид*\]</span><span class="sxs-lookup"><span data-stu-id="6e191-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="6e191-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="6e191-109">Part</span></span>     | <span data-ttu-id="6e191-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6e191-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="6e191-111">*модеид*</span><span class="sxs-lookup"><span data-stu-id="6e191-111">*ModeID*</span></span> | <span data-ttu-id="6e191-112">Строковое выражение, соответствующее ИДЕНТИФИКАТОРу режима обработчика речи.</span><span class="sxs-lookup"><span data-stu-id="6e191-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e191-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e191-113">Remarks</span></span>

<span data-ttu-id="6e191-114">Это свойство определяет идентификатор режима обработчика TTS (преобразование текста в речь) для речевого вывода символа.</span><span class="sxs-lookup"><span data-stu-id="6e191-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="6e191-115">Идентификатор режима для модуля TTS — это отформатированная строка, определяемая поставщиком речи, которая однозначно определяет режим работы механизма.</span><span class="sxs-lookup"><span data-stu-id="6e191-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="6e191-116">Дополнительные сведения см. [в разделе доступ к модулю распознавания речи в коде](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="6e191-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="6e191-117">Задание этого свойства переопределяет попытку сервера загрузить модуль на основе параметра TTS, скомпилированного символом, и текущего параметра [**LanguageID**](languageid-property.md) символа.</span><span class="sxs-lookup"><span data-stu-id="6e191-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="6e191-118">Однако если указать идентификатор режима для ядра, который не установлен, или если пользователь отключил речевой вывод на странице свойств Microsoft Agent (**аудиуутпут. Enabled = false**), сервер выдаст ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e191-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="6e191-119">Если вы не установили для символа идентификатор режима TTS (или не были успешно установлены), сервер проверяет, соответствует ли параметру режима TTS, заданному для символа, параметру [**LanguageID**](languageid-property.md) , и что соответствующий обработчик TTS установлен.</span><span class="sxs-lookup"><span data-stu-id="6e191-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="6e191-120">Если да, то режим TTS, используемый символом для выходного выхода, и это свойство возвращает идентификатор этого режима.</span><span class="sxs-lookup"><span data-stu-id="6e191-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="6e191-121">В противном случае сервер запрашивает совместимый речевой обработчик SAPI, соответствующий **LanguageID** символа, а также пол и Age, заданные для идентификатора скомпилированного режима символа.</span><span class="sxs-lookup"><span data-stu-id="6e191-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="6e191-122">Если не задан параметр **LanguageID** символа, его **LanguageID** является текущим языком пользователя.</span><span class="sxs-lookup"><span data-stu-id="6e191-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="6e191-123">Если соответствующий механизм не найден, запрос этого свойства возвращает пустую строку для идентификатора режима ядра.</span><span class="sxs-lookup"><span data-stu-id="6e191-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="6e191-124">Аналогичным образом, если вы запрашиваете это свойство, когда пользователь отключил речевой вывод на странице свойств Microsoft Agent (**аудиуутпут. Enabled = false**), значение будет пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="6e191-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="6e191-125">При запросе или задании этого свойства будет загружен соответствующий обработчик (если он еще не загружен).</span><span class="sxs-lookup"><span data-stu-id="6e191-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="6e191-126">Однако, если подсистема, указанная в параметре «скомпилированный символ», установлена и соответствует параметру идентификатора языка символа, подсистема будет загружена при загрузке символа.</span><span class="sxs-lookup"><span data-stu-id="6e191-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="6e191-127">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="6e191-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="6e191-128">Требования к речевому подсистему агента Microsoft Agent основаны на Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="6e191-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="6e191-129">Модули, поддерживающие требования к SAPI Microsoft Agent, можно установить и использовать с агентом.</span><span class="sxs-lookup"><span data-stu-id="6e191-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="6e191-130">Это свойство также возвращает пустую строку, если в системе не установлена совместимая поддержка звука.</span><span class="sxs-lookup"><span data-stu-id="6e191-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="6e191-131">Установка **ттсмодеид** может завершиться ошибкой, если не установлен Speech.dll и указанный модуль не соответствует параметру режима TTS, скомпилированному для символа.</span><span class="sxs-lookup"><span data-stu-id="6e191-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="6e191-132">Запрос этого свойства обычно не возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6e191-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="6e191-133">Тем не менее, если при загрузке обработчика речи занимает слишком много времени, может возникнуть ошибка, указывающая, что время ожидания запроса истекло.</span><span class="sxs-lookup"><span data-stu-id="6e191-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="6e191-134">См. также:</span><span class="sxs-lookup"><span data-stu-id="6e191-134">See Also</span></span>

[<span data-ttu-id="6e191-135">**LanguageID, свойство**</span><span class="sxs-lookup"><span data-stu-id="6e191-135">**LanguageID property**</span></span>](languageid-property.md)


 

 




