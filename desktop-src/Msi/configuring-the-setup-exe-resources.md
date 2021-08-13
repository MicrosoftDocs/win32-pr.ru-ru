---
description: настраиваемый исполняемый файл начальной загрузки (Setup.exe) и средство настройки (Msistuff.exe) входят в состав Windows SDK компонентов для установщик Windows разработчиков.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Настройка ресурсов Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638733"
---
# <a name="configuring-the-setupexe-resources"></a>Настройка ресурсов Setup.exe

настраиваемый исполняемый файл начальной загрузки (Setup.exe) и средство настройки ( [Msistuff.exe](msistuff-exe.md)) входят в состав [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md). используя Msistuff.exe для настройки ресурсов в Setup.exe, разработчики могут легко создать веб-установку пакета установщик Windows. Дополнительные сведения см. в разделе [начальная загрузка Интернета](internet-download-bootstrapping.md).

введите следующую командную строку, чтобы настроить ресурсы для образца, описанного в [примере установки установщик Windows на основе URL-адреса](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Продолжить](sign-setup-exe-and-mysetup-msi.md)

 

 



