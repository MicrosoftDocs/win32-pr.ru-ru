---
title: Проблемы установки и загрузки страниц
description: Проблемы установки и загрузки страниц
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77fb7a41578463364837281dffcdfb22177e9785673049a65f05e9d0e33240e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358881"
---
# <a name="installation-and-page-loading-problems"></a>Проблемы установки и загрузки страниц

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>при попытке установить microsoft Agent на microsoft Windows NT появляется сообщение о том, что мне нужно быть администратором.

Так как Microsoft Agent записывает файлы в системный каталог при установке, для установки требуются права администратора (не пользователя).

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>При попытке установить Microsoft Agent возникает одна из следующих ошибок: Process (regsvr32/s Windows \\ мсажент \\AgentCtl.dll). Ошибка при создании этого файла. Не удается найти этот файл. (Примечание. расположение каталога, упоминаемое в сообщении об ошибке, зависит от того, как вы установили Windows.) Требуемый MSVCRT.DLL DLL не найден. Ошибка при создании процесса <c: \\ Windows \\ мсажент \\agentsvr.exe/RegServer>. Причина: не удается найти один из файлов библиотеки, необходимых для запуска этого приложения. (Примечание. расположение каталога, упоминаемое в сообщении об ошибке, зависит от того, как вы установили Windows.)

Для установки Microsoft Agent требуется правильная установка Regsvr32.exe, Msvcrt.dll (библиотека времени выполнения Microsoft C) и обновленные DLL-библиотеки OLE. См. раздел обновление DCOM: ( <https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0> ). Лучший способ убедиться в наличии всех необходимых системных файлов — установить [Microsoft Internet Explorer 4,0](https://www.microsoft.com/ie/download) или более поздней версии.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>При попытке загрузить страницу, внесенную в скрипт для Microsoft Agent, возникает ошибка скрипта: "ошибка выполнения VBScript, требуется объект".

Одно из следующих условий может привести к отображению сообщения:

-   необходимо настроить параметры безопасности для Microsoft Internet Explorer, чтобы включить ActiveXные элементы управления и подключаемые модули. Проверьте страницу безопасности браузера. в Microsoft Internet Explorer откройте меню вид, выберите пункт параметры, перейдите на вкладку безопасность и убедитесь, что установлен флажок включить ActiveXные элементы управления и Plug-Ins.
-   вы работаете на компьютере с двойной загрузкой Windows 9x или Windows NT и установили Microsoft Agent на одной операционной системе, но пытаетесь получить доступ к странице из другой операционной системы. Несмотря на то, что операционные системы могут совместно использовать каталоги и файлы, данные реестра, используемые Microsoft Agent, не являются общими, поэтому необходимо установить Microsoft Agent в операционной системе, используемой для доступа к веб-страницам с помощью этого символа.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>При попытке загрузить страницу, написанную с помощью агента Microsoft Agent, ничего не происходит.

Это может произойти при наличии одного из следующих условий.

-   Проверьте параметры безопасности браузера. браузер должен быть настроен для включения загрузки сценариев ActiveX и воспроизведения ActiveX элементов управления.
-   При обращении к страницам, созданным с помощью Microsoft Agent и Microsoft Internet Explorer, требуется версия 3,02 или более поздняя (Скачайте последнюю версию Internet Explorer [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> ). В Microsoft Internet Explorer откройте меню вид, выберите пункт Параметры, перейдите на вкладку Безопасность и установите флажок все активные данные.
-   Эта ошибка также может быть вызвана Java-приложением на странице. Для запуска Microsoft Agent на той же странице, что и Java-приложение, требуется версия 2,0 виртуальной машины Майкрософт (VM). Дополнительные сведения см. в разделе [часто задаваемые вопросы по программированию и созданию сценариев](programming-scripting-faq.yml).

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>При попытке загрузить страницу, написанную с помощью агента Microsoft Agent, появляется сообщение "не удалось инициализировать Microsoft Agent".

Обычно это происходит, если у вас нет агента Майкрософт или какого-либо другого элемента управления, используемого страницей, и при появлении запроса на установку элемента управления выберите нет. Попробуйте обновить страницу, хотя страница может работать только в том случае, если установлены все необходимые компоненты.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>При попытке загрузить страницу, созданную с помощью агента Microsoft Agent, я получаю сообщение «компонент имеет цифровую подпись у своего издателя, но подпись не соответствует компоненту. Возможно, этот компонент был поврежден или изменен? Продолжить?".

Это может появиться при попытке установить Microsoft Agent в Microsoft Internet Explorer 3,02. Можно либо продолжить установку, либо обновить браузер до Internet Explorer 4,0 или более поздней версии.

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>При попытке загрузить страницу, внесенную в скрипт для Microsoft Agent с помощью Netscape Navigator (или других Интернет-браузеров), возникают ошибки.

Microsoft Agent реализуется с помощью интерфейсов ActiveX. его можно использовать только в браузере (например, в Microsoft Internet Explorer), поддерживающем внедрение ActiveX объектов с помощью сценария на странице и только в системах под управлением Microsoft Windows 95, Windows 98 и Windows NT 4,0 (или более поздней версии). если вы не используете Microsoft Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ), обратитесь к поставщику браузера за дополнительными сведениями о ActiveX support.

 

 




