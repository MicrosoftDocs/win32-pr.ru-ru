---
title: Иажентчарактерекс Жетттсмодеид
description: Иажентчарактерекс Жетттсмодеид
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069645"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="fcc6c-103">Иажентчарактерекс:: Жетттсмодеид</span><span class="sxs-lookup"><span data-stu-id="fcc6c-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="fcc6c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fcc6c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="fcc6c-105">Получает идентификатор режима для модуля TTS, заданного для символа.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="fcc6c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fcc6c-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*пбсзмодеид*</span><span class="sxs-lookup"><span data-stu-id="fcc6c-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="fcc6c-108">Адрес BSTR, принимающий параметр ID режима модуля TTS для символа.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="fcc6c-109">Этот параметр возвращает идентификатор режима TTS (преобразование текста в речь) для речевого вывода символа.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="fcc6c-110">Идентификатор режима для модуля TTS — это строковое представление GUID (в формате, заключенном в фигурные скобки и тире), определяемое поставщиком речи, которое однозначно определяет подсистему.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="fcc6c-111">Дополнительные сведения см. в [документации по Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="fcc6c-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="fcc6c-112">Запрос этого свойства приведет к загрузке связанного обработчика, если он еще не загружен.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="fcc6c-113">Если для символа не задан идентификатор режима TTS, сервер пытается вернуть подсистему, которая соответствует (с помощью интерфейсов API распознавания речи), параметр TTS для скомпилированного символа и текущий языковой параметр символа.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="fcc6c-114">Если они различаются, то параметр языка символа переопределяет параметр его автора.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="fcc6c-115">Если языковой параметр символа не задан, то языком символа будет идентификатор языка пользователя по умолчанию, а сервер попытается выполнить сопоставление на основе идентификатора этого языка.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="fcc6c-116">Эта функция не завершается ошибкой, если [**иажентаудиубжектпропертиес:: enable**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="fcc6c-117">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="fcc6c-118">Требования к речевому подсистему агента Microsoft Agent основаны на Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="fcc6c-119">Модули, поддерживающие требования к SAPI Microsoft Agent, можно установить и использовать с агентом.</span><span class="sxs-lookup"><span data-stu-id="fcc6c-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="fcc6c-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="fcc6c-120">See Also</span></span>

[<span data-ttu-id="fcc6c-121">**Иажентчарактерекс:: Сетттсмодеид**</span><span class="sxs-lookup"><span data-stu-id="fcc6c-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




