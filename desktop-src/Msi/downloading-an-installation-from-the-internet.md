---
description: Установщик Windows принимает универсальный указатель ресурсов (URL) в качестве допустимого источника для установки.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Загрузка установки из Интернета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650648"
---
# <a name="downloading-an-installation-from-the-internet"></a>Загрузка установки из Интернета

Установщик Windows принимает универсальный указатель ресурсов (URL) в качестве допустимого источника для установки. Установщик Windows может устанавливать пакеты, исправления и преобразования из расположения URL-адреса.

Если база данных установки находится по URL-адресу, установщик загружает базу данных в расположение кэша перед началом установки. Установщик также скачивает файлы и CAB-файлы из источника Интернета, которые подходят для выбора пользователя. Дополнительные сведения см. [в разделе Пример установки установщик Windows на основе URL-адресов](a-url-based-windows-installer-installation-example.md) .

Например, чтобы установить пакет с источником, расположенным на веб-сервере https://server/share/package.msi , можно использовать параметры [командной строки](command-line-options.md) для установки пакета и задания [общих](public-properties.md) свойств.

msiexec/i https://server/share/package.msi *свойство = значение*

Для запуска установки из веб-браузера необходимо передать в установщик командную строку, аналогичную показанной ранее. В общем случае не следует загружать и устанавливать пакет, просто дважды щелкнув MSI-файл в браузере. При этом MSI файл загружается в папку Temporary Internet Files и в установщик передается следующая команда:

**msiexec/i c: \\ \\ временные файлы интернета Windows \\package.msi**

Установка завершается сбоем, если пакету требуются внешние исходные файлы или ящики, так как они находятся не в том же расположении, что и MSI-файл.

Обратите внимание, что поскольку объект [**установщика**](installer-object.md) не помечен как [сафефорскриптинг](safeforscripting.md) на компьютере пользователя, пользователям необходимо изменить параметры безопасности браузера, чтобы пример работал правильно.

Метод [**инсталлпродукт**](installer-installproduct.md) можно использовать для запуска предыдущей команды из браузера в качестве события щелчка.


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



Обратите внимание, что поскольку некоторые веб-серверы чувствительны к регистру, поле FileName в таблице [File](file-table.md) должно точно соответствовать регистру исходных файлов, чтобы обеспечить поддержку загрузки из Интернета.

См. раздел [Загрузка и установка исправления из Интернета](downloading-and-installing-a-patch-from-the-internet.md). Дополнительные сведения о защите установки и использовании цифровых сертификатов см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей и установщик Windows](digital-signatures-and-windows-installer.md). Дополнительные сведения о создании веб-установки пакета установщик Windows см. в разделе [начальная загрузка Интернета](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Доступные протоколы Интернета

Начиная с Windows Server 2003 и Windows XP, установщик может использовать протоколы HTTP, HTTPS и FILE. Установщик не поддерживает протоколы FTP и GOPHER.

Установщик Windows версии 2,0 может использовать протоколы HTTP, FILE и FTP и не может использовать протоколы HTTPS и GOPHER.

 

 



