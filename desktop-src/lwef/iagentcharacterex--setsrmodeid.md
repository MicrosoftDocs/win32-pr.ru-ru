---
title: Иажентчарактерекс Сетсрмодеид
description: Иажентчарактерекс Сетсрмодеид
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487292"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="7744b-103">Иажентчарактерекс:: Сетсрмодеид</span><span class="sxs-lookup"><span data-stu-id="7744b-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="7744b-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7744b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="7744b-105">Задает идентификатор режима для модуля распознавания речи, заданный для символа.</span><span class="sxs-lookup"><span data-stu-id="7744b-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="7744b-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7744b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="7744b-107">бсзмодеид</span><span class="sxs-lookup"><span data-stu-id="7744b-107">bszModeID</span></span>

<span data-ttu-id="7744b-108">Параметр ID режима для модуля распознавания речи для символа.</span><span class="sxs-lookup"><span data-stu-id="7744b-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="7744b-109">Этот параметр задает подсистему для речевого ввода символа.</span><span class="sxs-lookup"><span data-stu-id="7744b-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="7744b-110">Идентификатор режима для модуля распознавания речи — это идентификатор GUID, определяемый поставщиком речи, который однозначно определяет режим работы механизма (отформатированный с помощью фигурных скобок и дефисов).</span><span class="sxs-lookup"><span data-stu-id="7744b-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="7744b-111">Дополнительные сведения см. в [документации по Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="7744b-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="7744b-112">Если указать идентификатор режима, который не соответствует параметру языка символа, если пользователь отключил распознавание речи (на странице свойств Microsoft Agent) или модуль не установлен, этот вызов завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="7744b-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="7744b-113">Если для символа не задан идентификатор режима модуля распознавания речи, сервер устанавливает тот, который соответствует языковому параметру символа (с помощью интерфейсов API распознавания речи Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="7744b-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="7744b-114">Если речевой ввод включен на странице свойств агента (дополнительные параметры символов), задание этого свойства приведет к загрузке связанного обработчика (если он еще не загружен) и запуск служб распознавания речи.</span><span class="sxs-lookup"><span data-stu-id="7744b-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="7744b-115">Это значит, что ключ прослушивания доступен и подсказка прослушивания доступна для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7744b-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="7744b-116">(Ключ прослушивания и TIP прослушивания включены, только если они также включены в дополнительных параметрах символов.) Однако если вы запрашиваете свойство, когда речь отключена, сервер не запускает речевые службы.</span><span class="sxs-lookup"><span data-stu-id="7744b-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="7744b-117">Это свойство применяется только к клиенту символа; параметр не отражает параметр других клиентов символа или других символов клиента.</span><span class="sxs-lookup"><span data-stu-id="7744b-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="7744b-118">Требования к речевому подсистему агента Microsoft Agent основаны на Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="7744b-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="7744b-119">Модули, поддерживающие требования к SAPI Microsoft Agent, можно установить и использовать с агентом.</span><span class="sxs-lookup"><span data-stu-id="7744b-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="7744b-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="7744b-120">See Also</span></span>

[<span data-ttu-id="7744b-121">**Иажентчарактерекс:: Жетсрмодеид**</span><span class="sxs-lookup"><span data-stu-id="7744b-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




