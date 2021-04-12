---
description: Microsoft установщик Windows принимает URL-адрес в качестве допустимого источника для исправления.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Загрузка и установка исправления из Интернета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154822"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Загрузка и установка исправления из Интернета

Microsoft установщик Windows принимает URL-адрес в качестве допустимого источника для [исправления](patch-packages.md). Чтобы установить исправление, расположенное на веб-сервере https://MyWeb/MyPatch.msp , используйте следующую командную строку:

**msiexec/p https://MyWeb/MyPatch.msp**

Чтобы избежать непредвиденных результатов, не запускайте исправление, щелкнув ссылку на веб-странице, на которой отображается URL-адрес файла исправления. Также можно установить исправление с помощью сценария, как в следующем примере:


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



Обратите внимание, что поскольку объект [**установщика**](installer-object.md) не помечен как [сафефорскриптинг](safeforscripting.md) на компьютере пользователя, пользователям необходимо изменить параметры безопасности браузера, чтобы пример работал правильно.

Дополнительные сведения см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей и установщик Windows](digital-signatures-and-windows-installer.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Пакеты исправлений](patch-packages.md)
</dt> <dt>

[Создание пакета исправлений](creating-a-patch-package.md)
</dt> <dt>

[Исправление настроенных приложений](patching-customized-applications.md)
</dt> <dt>

[Загрузка установки из Интернета](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



