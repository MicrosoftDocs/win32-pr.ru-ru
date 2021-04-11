---
description: Последним шагом является размещение ссылки на Setup.exe на гипотетической веб-странице MySetup (MySetup.html), описанной в примере установки установщик Windows на основе URL-адреса.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Установка ссылки HTML на Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264848"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Установка ссылки HTML на Setup.exe

Последним шагом является размещение ссылки на Setup.exe на гипотетической веб-странице MySetup (MySetup.html), описанной в [примере установки установщик Windows на основе URL-адреса](a-url-based-windows-installer-installation-example.md). Используйте следующий скрипт HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Если щелкнуть ссылку "Установка MySetup", пользователи смогут сохранить или запустить из этого расположения. Если пользователь выбирает Запуск из этого расположения, Setup.exe обновляет версию установщик Windows на компьютере, при необходимости проверяет цифровую подпись в пакете установщика и устанавливает пакет на своем компьютере.

Это завершает пример.

 

 



