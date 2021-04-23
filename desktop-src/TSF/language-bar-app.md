---
title: Языковая панель (приложения TSF)
description: Приложение не может добавлять элементы на языковую панель; только служба текстового ввода может добавлять элементы на языковую панель.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Платформа текстовых служб (TSF), языковая панель
- TSF (платформа текстовых служб), языковая панель
- Приложения с поддержкой TSF, языковая панель
- Языковая панель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891373"
---
# <a name="language-bar-tsf-applications"></a><span data-ttu-id="d5d64-107">Языковая панель (приложения TSF)</span><span class="sxs-lookup"><span data-stu-id="d5d64-107">Language Bar (TSF Applications)</span></span>

<span data-ttu-id="d5d64-108">Приложение не может добавлять элементы на языковую панель; только служба текстового ввода может добавлять элементы на языковую панель.</span><span class="sxs-lookup"><span data-stu-id="d5d64-108">An application cannot add items to the language bar; only a text service can add items to the language bar.</span></span> <span data-ttu-id="d5d64-109">Приложение может повлиять на отображение определенных элементов на языковой панели.</span><span class="sxs-lookup"><span data-stu-id="d5d64-109">An application can affect how certain items on the language bar appear.</span></span>

<span data-ttu-id="d5d64-110">Для указания типа речевого ввода, который может принимать приложение: прямой ввод текста (Диктовка) и/или голосовые команды, используется [ \_ \_ \_ диктатионстатая Секция GUID секции](predefined-compartments.md) .</span><span class="sxs-lookup"><span data-stu-id="d5d64-110">The [GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT](predefined-compartments.md) compartment is used to indicate the type of speech input that the application can accept: direct text input (dictation) and/or voice commands.</span></span> <span data-ttu-id="d5d64-111">По умолчанию режим диктовки включен, а команда Voice отключена.</span><span class="sxs-lookup"><span data-stu-id="d5d64-111">By default, dictation is enabled and voice command is disabled.</span></span> <span data-ttu-id="d5d64-112">Если приложение может принимать голосовые команды, оно должно задавать значение [ \_ \_ Enabled для поддержки команд TF](speech-recognition-constants.md) в секции GUID диктатионстат в модуле " \_ речь" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d5d64-112">If the application can accept voice commands, it should set the [TF\_COMMANDING\_ENABLED](speech-recognition-constants.md) value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="d5d64-113">Если приложение может принимать диктовку, оно должно устанавливать значение "TF \_ Dictation \_ Enabled" в секции GUID диктатионстат в модуле " \_ речь" \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d5d64-113">If the application can accept dictation, it should set the TF\_DICTATION\_ENABLED value in the GUID\_COMPARTMENT\_SPEECH\_DICTATIONSTAT compartment.</span></span> <span data-ttu-id="d5d64-114">Параметр TF \_ Dictation \_ On или TF \_ Command by \_ On value этой секции определяет, в какой режим (Диктовка или команда) речевое входное значение в настоящее время находится в.</span><span class="sxs-lookup"><span data-stu-id="d5d64-114">The TF\_DICTATION\_ON or TF\_COMMANDING\_ON value of this compartment determines which mode (dictation or command) speech input is currently in.</span></span>

<span data-ttu-id="d5d64-115">Если приложение поддерживает постоянное хранение данных свойств, оно должно задавать ненулевое значение для секции [ \_ \_ персистменуенаблед секции GUID](predefined-compartments.md) .</span><span class="sxs-lookup"><span data-stu-id="d5d64-115">If the application supports persistent storage of property data, it should set the [GUID\_COMPARTMENT\_PERSISTMENUENABLED](predefined-compartments.md) compartment to a nonzero value.</span></span> <span data-ttu-id="d5d64-116">В результате служба речевого текста включит пункт меню **сохранить речевые данные** .</span><span class="sxs-lookup"><span data-stu-id="d5d64-116">This causes the speech text service to enable the **Save Speech Data** menu item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5d64-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d5d64-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5d64-118">Как настроить платформу текстовых служб</span><span class="sxs-lookup"><span data-stu-id="d5d64-118">How To Set Up Text Services Framework</span></span>](how-to-set-up-tsf.md)
</dt> <dt>

[<span data-ttu-id="d5d64-119">Языковая панель (текстовые службы)</span><span class="sxs-lookup"><span data-stu-id="d5d64-119">Language Bar (Text Services)</span></span>](language-bar.md)
</dt> </dl>

 

 




