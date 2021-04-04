---
title: Иажентчарактерекс Жетсрмодеид
description: Иажентчарактерекс Жетсрмодеид
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103789000"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="91430-103">Иажентчарактерекс:: Жетсрмодеид</span><span class="sxs-lookup"><span data-stu-id="91430-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="91430-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="91430-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="91430-105">Получает идентификатор режима для модуля распознавания речи, заданного для символа.</span><span class="sxs-lookup"><span data-stu-id="91430-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="91430-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="91430-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="91430-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*пбсзмодеид*</span><span class="sxs-lookup"><span data-stu-id="91430-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="91430-108">Адрес BSTR, который получает значение параметра идентификатора режима модуля распознавания речи для символа.</span><span class="sxs-lookup"><span data-stu-id="91430-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="91430-109">Этот параметр возвращает набор ядер для речевого ввода символа.</span><span class="sxs-lookup"><span data-stu-id="91430-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="91430-110">Идентификатор режима для модуля распознавания речи — это строковое представление идентификатора GUID (в формате, заключенном в фигурные скобки и дефисы) поставщиком речи, который однозначно определяет подсистему.</span><span class="sxs-lookup"><span data-stu-id="91430-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="91430-111">Дополнительные сведения см. в [документации по Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="91430-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="91430-112">Если для символа не задан идентификатор режима модуля распознавания речи, сервер возвращает подсистему, соответствующую языковому параметру символа (с помощью интерфейсов API распознавания речи Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="91430-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="91430-113">Если для символа не существует соответствующего механизма распознавания речи, сервер возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="91430-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="91430-114">Если речевой ввод включен (в окне Дополнительные параметры символов), при запросе или задании этого свойства будет загружен соответствующий обработчик (если он еще не загружен) и запущены службы речи.</span><span class="sxs-lookup"><span data-stu-id="91430-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="91430-115">Это значит, что ключ прослушивания доступен и подсказка прослушивания доступна для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="91430-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="91430-116">(Ключ прослушивания и TIP прослушивания включены, только если они также включены в дополнительных параметрах символов.) Однако если вы запрашиваете свойство, когда речь отключена, сервер не запускает речевые службы и возвращает пустую строку (пустую строку).</span><span class="sxs-lookup"><span data-stu-id="91430-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="91430-117">Эта функция возвращает только параметр для использования символа в клиентском приложении. параметр не отражает другие клиенты символов или другие символы клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="91430-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="91430-118">Эта функция не завершается ошибкой, если [**иажентспичинпутпропертиес:: enable**](iagentspeechinputproperties--getenabled.md) возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="91430-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="91430-119">Требования к речевому подсистему агента Microsoft Agent основаны на Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="91430-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="91430-120">Модули, поддерживающие требования к SAPI Microsoft Agent, можно установить и использовать с агентом.</span><span class="sxs-lookup"><span data-stu-id="91430-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="91430-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="91430-121">See Also</span></span>

[<span data-ttu-id="91430-122">**Иажентчарактерекс:: Сетсрмодеид**</span><span class="sxs-lookup"><span data-stu-id="91430-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




