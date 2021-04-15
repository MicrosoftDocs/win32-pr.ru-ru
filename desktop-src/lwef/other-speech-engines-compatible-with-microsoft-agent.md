---
title: Другие обработчики речи, совместимые с Microsoft Agent
description: Другие обработчики речи, совместимые с Microsoft Agent
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412605"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a><span data-ttu-id="60f67-103">Другие обработчики речи, совместимые с Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="60f67-103">Other Speech Engines Compatible with Microsoft Agent</span></span>

<span data-ttu-id="60f67-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60f67-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="60f67-105">Помимо обработчиков речи Майкрософт, поставляемых с и поддерживающих Microsoft Agent, некоторые компании также предлагают речевые модули с поддержкой Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="60f67-105">In addition to the Microsoft speech engines that are provided with and support Microsoft Agent, a number of companies also offer speech engines with support for Microsoft Agent.</span></span> <span data-ttu-id="60f67-106">На этой странице представлен краткий обзор таких ядер, которые могут быть доступны на английском языке (США) и других языках.</span><span class="sxs-lookup"><span data-stu-id="60f67-106">This page gives you a brief overview of such engines that may be available in U.S. English and other languages.</span></span> <span data-ttu-id="60f67-107">Сведения об установке и доступе, а также о лицензировании и повторном распространении модулей можно найти на веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="60f67-107">Information about how to install and access, as well as license and redistribute the engines can be found at their websites.</span></span>

<span data-ttu-id="60f67-108">При использовании любого стороннего модуля распознавания речи также необходимо установить Microsoft SAPI 4.0 двоичные файлы среды выполнения, чтобы модули были перечислены правильно.</span><span class="sxs-lookup"><span data-stu-id="60f67-108">When using any third-party speech engine, you also need to install Microsoft SAPI 4.0a runtime binaries so that the engines are enumerated properly.</span></span> <span data-ttu-id="60f67-109">На веб-странице можно включить следующий тег, чтобы активировать автозагрузку API распознавания речи:</span><span class="sxs-lookup"><span data-stu-id="60f67-109">From your webpage you can include the following tag to trigger an autodownload of the Speech API:</span></span>

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

<span data-ttu-id="60f67-110">Дополнительные сведения о двоичных файлах среды выполнения SAPI см. на [веб-сайте группы речи Майкрософт](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="60f67-110">For more information about the SAPI runtime binaries, refer to the [Microsoft Speech group's website](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="60f67-111">Microsoft Agent также устанавливает двоичные файлы среды выполнения SAPI с помощью модуля распознавания речи Майкрософт, панели управления речевыми файлами и редактора символов агента.</span><span class="sxs-lookup"><span data-stu-id="60f67-111">Microsoft Agent also installs the SAPI runtime binaries with the Microsoft Speech Recognition Engine, the Speech Control Panel, and the Agent Character Editor.</span></span>

<span data-ttu-id="60f67-112">Обратите внимание, что эти ссылки указывают на серверы, которые не находятся под контролем Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="60f67-112">Please note that these links point to servers that are not under Microsoft control.</span></span> <span data-ttu-id="60f67-113">Ознакомьтесь с [официальной инструкцией](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) Майкрософт относительно других серверов.</span><span class="sxs-lookup"><span data-stu-id="60f67-113">Please read the Microsoft [official statement](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) regarding other servers.</span></span> <span data-ttu-id="60f67-114">Корпорация Майкрософт не подтверждает содержимое и программное обеспечение, предоставленное на этих веб-сайтах.</span><span class="sxs-lookup"><span data-stu-id="60f67-114">Microsoft does not endorse the content nor the software provided at these websites.</span></span> <span data-ttu-id="60f67-115">Все технические вопросы и ответы на техническую поддержку должны также направляться поставщикам ядер, а не корпорации Майкрософт или группе Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="60f67-115">All technical and support questions should also be directed to the suppliers of the engines and not to Microsoft or the Microsoft Agent team.</span></span>

<span data-ttu-id="60f67-116">**Модуль преобразования текста в речь для дигало**</span><span class="sxs-lookup"><span data-stu-id="60f67-116">**Digalo Text-To-Speech Engine**</span></span>

<span data-ttu-id="60f67-117">Дигало — это недорогой модуль TTS, предназначенный для конечных пользователей и разработчиков.</span><span class="sxs-lookup"><span data-stu-id="60f67-117">Digalo is an affordable TTS engine designed for end-users and developers.</span></span> <span data-ttu-id="60f67-118">Этот механизм предлагается на нескольких языках: на французском, немецком, португальском (Бразилия), испанском, русском, французском и американском США, а также на итальянском, польском и других языках.</span><span class="sxs-lookup"><span data-stu-id="60f67-118">The engine is offered in a number of languages: French, German, Portuguese (Brazil), Spanish, Russian, and UK and U.S. English, with Italian, Polish, and other languages coming soon.</span></span> <span data-ttu-id="60f67-119">Также доступна информация для разработчиков, а также сведения о регистрации и связанных с конечным пользователем программах.</span><span class="sxs-lookup"><span data-stu-id="60f67-119">Developer information, as well as details on end-user registration and affiliate programs, is also available.</span></span>

<span data-ttu-id="60f67-120">**Модуль распознавания речи Elan**</span><span class="sxs-lookup"><span data-stu-id="60f67-120">**Elan Speech Engine**</span></span>

<span data-ttu-id="60f67-121">Модуль распознавания речи Elan использует технологию преобразования текста Elan в речь и доступен на семи языках: французский, немецкий, португальский (Бразилия), испанский, Русский, Великобритания и английский (США).</span><span class="sxs-lookup"><span data-stu-id="60f67-121">Elan Speech Engine uses Elan's Text To Speech technology and is available in seven languages: French, German, Portuguese (Brazil), Spanish, Russian, UK and U.S. English.</span></span>

<span data-ttu-id="60f67-122">**IBM Виавоице**</span><span class="sxs-lookup"><span data-stu-id="60f67-122">**IBM ViaVoice Outloud**</span></span>

<span data-ttu-id="60f67-123">Компания IBM разработала несколько символов Microsoft Agent для использования с Виавоице.</span><span class="sxs-lookup"><span data-stu-id="60f67-123">IBM has developed several Microsoft Agent characters for use with ViaVoice Outloud.</span></span> <span data-ttu-id="60f67-124">IBM Виавоице — это технология преобразования текста в речь, которая доступна на французском, немецком, итальянском, испанском, Великобритании и американском английском.</span><span class="sxs-lookup"><span data-stu-id="60f67-124">IBM ViaVoice Outloud is a text-to-speech (speech synthesis) technology and is available in French, German, Italian, Spanish, UK English and U.S. English.</span></span> <span data-ttu-id="60f67-125">В сочетании с Microsoft Agent вы можете создавать насыщенные приложения на многих языках и расширять возможности продаж на новые мировые рынки.</span><span class="sxs-lookup"><span data-stu-id="60f67-125">When combined with Microsoft Agent, you can create vibrant applications in many languages and extend your sales opportunities to new worldwide markets.</span></span>

 

 




