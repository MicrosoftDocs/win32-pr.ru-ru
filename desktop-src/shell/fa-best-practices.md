---
description: Ниже приведены рекомендуемые рекомендации, которые следует использовать при работе с сопоставлениями файлов.
title: Рекомендации по сопоставлению файлов
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d4d0edf9-3475-4164-b0fa-15006e05e242
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f49c1df6d145c32b8fcbdf70462b30f14f51b3d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541087"
---
# <a name="best-practices-for-file-associations"></a><span data-ttu-id="401b0-103">Рекомендации по сопоставлению файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-103">Best Practices for File Associations</span></span>

<span data-ttu-id="401b0-104">Ниже приведены рекомендуемые рекомендации, которые следует использовать при работе с сопоставлениями файлов.</span><span class="sxs-lookup"><span data-stu-id="401b0-104">The following list are recommended best practices you should use when working with file associations.</span></span>

-   [<span data-ttu-id="401b0-105">Не копировать сопоставлений файлов из реестра</span><span class="sxs-lookup"><span data-stu-id="401b0-105">Do Not Copy File Associations from the Registry</span></span>](#do-not-copy-file-associations-from-the-registry)
-   [<span data-ttu-id="401b0-106">Старайтесь не Hard-Coding пути в реестр, когда это возможно</span><span class="sxs-lookup"><span data-stu-id="401b0-106">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>](#avoid-hard-coding-paths-into-the-registry-where-possible)
-   [<span data-ttu-id="401b0-107">Всегда переносить развернутые строки в кавычки</span><span class="sxs-lookup"><span data-stu-id="401b0-107">Always Wrap Expanding Strings in Quotation Marks</span></span>](#always-wrap-expanding-strings-in-quotation-marks)
-   [<span data-ttu-id="401b0-108">Не путать автозапуск и Автозагрузка с сопоставлениями файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-108">Do Not Confuse Autoplay/Autorun with File Associations</span></span>](#do-not-confuse-autoplayautorun-with-file-associations)
-   [<span data-ttu-id="401b0-109">Не путайте базу данных MIME Internet Explorer с сопоставлениями файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-109">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>](#do-not-confuse-the-internet-explorer-mime-database-with-file-associations)
-   [<span data-ttu-id="401b0-110">Использование правильно сформированных и версий ProgID</span><span class="sxs-lookup"><span data-stu-id="401b0-110">Use Properly Formed and Versioned ProgIDs</span></span>](#use-properly-formed-and-versioned-progids)
-   [<span data-ttu-id="401b0-111">Не использовать короткие расширения имен файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-111">Do Not Use Short File Name Extensions</span></span>](#do-not-use-short-file-name-extensions)
-   [<span data-ttu-id="401b0-112">Регистрация новых типов файлов в базе данных MIME IANA</span><span class="sxs-lookup"><span data-stu-id="401b0-112">Register New File Types in the IANA MIME Database</span></span>](#register-new-file-types-in-the-iana-mime-database)
-   [<span data-ttu-id="401b0-113">Регистрация в веб-службе Windows для сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-113">Sign Up with the Windows Web Service for File Associations</span></span>](#sign-up-with-the-windows-web-service-for-file-associations)
-   [<span data-ttu-id="401b0-114">См. также</span><span class="sxs-lookup"><span data-stu-id="401b0-114">Related topics</span></span>](#related-topics)

## <a name="do-not-copy-file-associations-from-the-registry"></a><span data-ttu-id="401b0-115">Не копировать сопоставлений файлов из реестра</span><span class="sxs-lookup"><span data-stu-id="401b0-115">Do Not Copy File Associations from the Registry</span></span>

<span data-ttu-id="401b0-116">Рекомендуется не копировать существующие сопоставления файлов из реестра.</span><span class="sxs-lookup"><span data-stu-id="401b0-116">We recommended that you do not copy existing file associations from the registry.</span></span> <span data-ttu-id="401b0-117">Это часто приводит к распространению сопоставлений плохо сформированных файлов.</span><span class="sxs-lookup"><span data-stu-id="401b0-117">This often leads to the propagation of poorly formed file associations.</span></span> <span data-ttu-id="401b0-118">Вместо этого следует выполнить действия, описанные в [примере сценария сопоставления файлов](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="401b0-118">Instead, you should follow the steps outlined in [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

## <a name="avoid-hard-coding-paths-into-the-registry-where-possible"></a><span data-ttu-id="401b0-119">Старайтесь не Hard-Coding пути в реестр, когда это возможно</span><span class="sxs-lookup"><span data-stu-id="401b0-119">Avoid Hard-Coding Paths into the Registry Where Possible</span></span>

<span data-ttu-id="401b0-120">Так же, как жестко запрограммированные пути к программам могут вызвать проблемы, при работе с жестко написанием путей в реестре могут возникнуть проблемы.</span><span class="sxs-lookup"><span data-stu-id="401b0-120">Just as hard-coding paths into programs can cause problems, hard-coding paths into the registry can also lead to problems.</span></span> <span data-ttu-id="401b0-121">Вместо этого следует использовать строки расширения реестра (REG \_ expand \_ SZ), чтобы обеспечить независимость от пути там, где это применимо.</span><span class="sxs-lookup"><span data-stu-id="401b0-121">Instead, you should use registry expansion strings (REG\_EXPAND\_SZ) to provide path independence where applicable.</span></span> <span data-ttu-id="401b0-122">Например, вместо использования этого метода:</span><span class="sxs-lookup"><span data-stu-id="401b0-122">For example, instead of using this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = C:\WINNT\hta.exe,1
```

<span data-ttu-id="401b0-123">Этот метод следует использовать:</span><span class="sxs-lookup"><span data-stu-id="401b0-123">You should use this method:</span></span>

```
HKEY_CLASSES_ROOT
   MyVendor.MyProgram.1
      DefaultIcon
         (Default) = "%SYSTEMROOT%\hta.exe,1"
```

## <a name="always-wrap-expanding-strings-in-quotation-marks"></a><span data-ttu-id="401b0-124">Всегда переносить развернутые строки в кавычки</span><span class="sxs-lookup"><span data-stu-id="401b0-124">Always Wrap Expanding Strings in Quotation Marks</span></span>

<span data-ttu-id="401b0-125">При развертывании строки могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="401b0-125">Expanding strings can contain spaces when they expand.</span></span> <span data-ttu-id="401b0-126">Поскольку пробелы часто обрабатываются как разделители аргументов, они вызывают проблемы при определенных обстоятельствах.</span><span class="sxs-lookup"><span data-stu-id="401b0-126">Because spaces are often interpreted as argument delimiters, they cause problems under certain circumstances.</span></span> <span data-ttu-id="401b0-127">Например, команда для вызова MyProgram может храниться в реестре следующим образом:</span><span class="sxs-lookup"><span data-stu-id="401b0-127">For example, a command to invoke MyProgram can be stored in the registry as:</span></span>

`%SYSTEMROOT%\MyProgram %1 %2`

<span data-ttu-id="401b0-128">MyProgram ждет, что %1 является полным путем к имени файла, а %2 — параметром, указывающим на какое-либо действие.</span><span class="sxs-lookup"><span data-stu-id="401b0-128">MyProgram expects that %1 is the full path to a file name, and %2 is a switch to indicate some action.</span></span> <span data-ttu-id="401b0-129">Если эта команда выполняется с аргументами **C: \\ Program Files \\ Мои документы \\document.txt** и **/принт** и предполагается наличие корневого каталога C: \\ WinNT, он расширяется до:</span><span class="sxs-lookup"><span data-stu-id="401b0-129">If this command is executed with arguments **C:\\Program Files\\My Documents\\document.txt** and **/print**, and assuming a SYSTEMROOT of C:\\WINNT, it expands to:</span></span>

`C:\WINNT\MyProgram C:\Program Files\My Documents\document.txt /print`

<span data-ttu-id="401b0-130">В этом случае MyProgram интерпретирует, что первый аргумент имеет значение C: \\ Program, а второй аргумент — файлы \\ My, что не является предполагаемым поведением.</span><span class="sxs-lookup"><span data-stu-id="401b0-130">In this case, MyProgram interprets that the first argument is C:\\Program, and the second argument is Files\\My, which is not the intended behavior.</span></span> <span data-ttu-id="401b0-131">Эти аргументы правильно интерпретируемы, независимо от того, содержат ли они пробелы, если развернутые строки заключены в кавычки следующим образом:</span><span class="sxs-lookup"><span data-stu-id="401b0-131">The arguments are interpreted correctly, however, regardless of whether they contain spaces, if the expanding strings are wrapped in quotation marks as follows:</span></span>

`"%SYSTEMROOT%\MyProgram" "%1" "%2"`

## <a name="do-not-confuse-autoplayautorun-with-file-associations"></a><span data-ttu-id="401b0-132">Не путать автозапуск и Автозагрузка с сопоставлениями файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-132">Do Not Confuse Autoplay/Autorun with File Associations</span></span>

<span data-ttu-id="401b0-133">В некоторых случаях сопоставления файлов аналогичны средствам автозапуска и автозапуска.</span><span class="sxs-lookup"><span data-stu-id="401b0-133">File Associations are similar to Autoplay/Autorun in some ways.</span></span> <span data-ttu-id="401b0-134">Однако автозапуск и Автозагрузка предлагают отдельные и разные средства, предоставляемые связями файлов.</span><span class="sxs-lookup"><span data-stu-id="401b0-134">However, Autoplay/Autorun offers separate and distinct facilities from those provided by file associations.</span></span> <span data-ttu-id="401b0-135">Дополнительные сведения см. [в статье Создание приложения для чтения компакт-дисков с поддержкой автозапуска](autoplay.md).</span><span class="sxs-lookup"><span data-stu-id="401b0-135">For more information see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md).</span></span>

## <a name="do-not-confuse-the-internet-explorer-mime-database-with-file-associations"></a><span data-ttu-id="401b0-136">Не путайте базу данных MIME Internet Explorer с сопоставлениями файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-136">Do Not Confuse the Internet Explorer MIME Database with File Associations</span></span>

<span data-ttu-id="401b0-137">Сопоставления файлов похожи на базу данных MIME Windows Internet Explorer. в этих типах файлов могут содержаться определения типов MIME (и должны).</span><span class="sxs-lookup"><span data-stu-id="401b0-137">File Associations are similar to the Windows Internet Explorer MIME database, in that file types can (and should) include a MIME type definition.</span></span> <span data-ttu-id="401b0-138">Однако база данных MIME Internet Explorer является отдельной и отличается от сопоставлений файлов.</span><span class="sxs-lookup"><span data-stu-id="401b0-138">However, the Internet Explorer MIME database is separate and distinct from file associations.</span></span>

## <a name="use-properly-formed-and-versioned-progids"></a><span data-ttu-id="401b0-139">Использование правильно сформированных и версий ProgID</span><span class="sxs-lookup"><span data-stu-id="401b0-139">Use Properly Formed and Versioned ProgIDs</span></span>

<span data-ttu-id="401b0-140">Всегда используйте [версии ProgID](fa-progids.md), даже если существует только одна версия ProgID.</span><span class="sxs-lookup"><span data-stu-id="401b0-140">Always use [versioned ProgIDs](fa-progids.md), even if there is only one version of the ProgID.</span></span> <span data-ttu-id="401b0-141">С помощью версий ProgID можно избежать конфликтов ProgID и перезаписи.</span><span class="sxs-lookup"><span data-stu-id="401b0-141">Versioned ProgIDs help to avoid ProgID conflicts and overwrites.</span></span> <span data-ttu-id="401b0-142">Они также позволяют использовать различные версии приложения для совместного существования.</span><span class="sxs-lookup"><span data-stu-id="401b0-142">They also enable different versions of an application to co-exist.</span></span>

## <a name="do-not-use-short-file-name-extensions"></a><span data-ttu-id="401b0-143">Не использовать короткие расширения имен файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-143">Do Not Use Short File Name Extensions</span></span>

<span data-ttu-id="401b0-144">Длинные расширения имен файлов предлагают следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="401b0-144">Long file name extensions offer the following advantages:</span></span>

-   <span data-ttu-id="401b0-145">Ограниченная длина коротких расширений делает их подверженными *конфликтам расширений.*</span><span class="sxs-lookup"><span data-stu-id="401b0-145">The limited length of short extensions make them prone to *extension collisions.*</span></span> <span data-ttu-id="401b0-146">Конфликты расширений возникают, когда одно и то же расширение используется для классификации нескольких типов файлов.</span><span class="sxs-lookup"><span data-stu-id="401b0-146">An extension collision occurs when the same extension is used to classify multiple file types.</span></span> <span data-ttu-id="401b0-147">Использование длинных расширений значительно снижает вероятность конфликта.</span><span class="sxs-lookup"><span data-stu-id="401b0-147">Using long extensions significantly decreases the chances of a collision.</span></span>
-   <span data-ttu-id="401b0-148">Короткие имена файлов, скорее всего, несколько понятны.</span><span class="sxs-lookup"><span data-stu-id="401b0-148">Short file names tend to be somewhat cryptic.</span></span> <span data-ttu-id="401b0-149">Длинные расширения, как правило, являются более осмысленными, так как дополнительные сведения можно внедрять в расширение.</span><span class="sxs-lookup"><span data-stu-id="401b0-149">Long extensions tend to be more meaningful because additional information can be embedded in the extension.</span></span>

<span data-ttu-id="401b0-150">Дополнительные сведения см. в разделе [расширения имен файлов](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="401b0-150">For more information, see [file name extensions](fa-file-extensions.md).</span></span>

## <a name="register-new-file-types-in-the-iana-mime-database"></a><span data-ttu-id="401b0-151">Регистрация новых типов файлов в базе данных MIME IANA</span><span class="sxs-lookup"><span data-stu-id="401b0-151">Register New File Types in the IANA MIME Database</span></span>

<span data-ttu-id="401b0-152">Центр назначенных номеров Интернета (IANA) хранит общедоступную базу данных зарегистрированных типов MIME.</span><span class="sxs-lookup"><span data-stu-id="401b0-152">The Internet Assigned Numbers Authority (IANA) keeps a public database of registered MIME types.</span></span> <span data-ttu-id="401b0-153">При определении нового типа общедоступного файла рекомендуется также определить тип MIME для типа файла и зарегистрировать этот тип в IANA.</span><span class="sxs-lookup"><span data-stu-id="401b0-153">When defining a new public file type, we recommended that you also define a MIME type for the file type and register this type with the IANA.</span></span> <span data-ttu-id="401b0-154">Нет затрат на регистрацию.</span><span class="sxs-lookup"><span data-stu-id="401b0-154">There is no cost for registration.</span></span>

## <a name="sign-up-with-the-windows-web-service-for-file-associations"></a><span data-ttu-id="401b0-155">Регистрация в веб-службе Windows для сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-155">Sign Up with the Windows Web Service for File Associations</span></span>

<span data-ttu-id="401b0-156">Разработчики приложений могут зарегистрироваться в веб-службе Windows, которую пользователи используют для поиска приложений, которые могут работать с файлами конкретного типа.</span><span class="sxs-lookup"><span data-stu-id="401b0-156">Application developers can sign up with the Windows Web Service that users use to find applications that can operate on specific file types.</span></span> <span data-ttu-id="401b0-157">Процесс регистрации в веб-службе подробно описан в процессе встроенной [системы сопоставления файлов Windows](https://support.microsoft.com/kb/929149).</span><span class="sxs-lookup"><span data-stu-id="401b0-157">The process for signing up with the web service is detailed in [Windows File Association System on-boarding process](https://support.microsoft.com/kb/929149).</span></span>

## <a name="related-topics"></a><span data-ttu-id="401b0-158">См. также</span><span class="sxs-lookup"><span data-stu-id="401b0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="401b0-159">Пример сценария сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="401b0-159">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="401b0-160">Рекомендации по управлению приложениями по умолчанию в Windows Vista и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="401b0-160">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="401b0-161">Программы по умолчанию</span><span class="sxs-lookup"><span data-stu-id="401b0-161">Default Programs</span></span>](default-programs.md)
</dt> <dt>

[<span data-ttu-id="401b0-162">Настройка доступа к программе и параметров по умолчанию для компьютера (SPAD)</span><span class="sxs-lookup"><span data-stu-id="401b0-162">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 



