---
description: последним шагом является размещение ссылки на Setup.exe на гипотетической веб-странице MySetup (MySetup.html), описанной в примере установки установщик Windows на основе URL-адреса.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Установка ссылки HTML на Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22be693c4e2e411fa724a70f90da4af4af4cf17ad6bb316bd3a483dd55bfd5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378074"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Установка ссылки HTML на Setup.exe

последним шагом является размещение ссылки на Setup.exe на гипотетической веб-странице MySetup (MySetup.html), описанной в [примере установки установщик Windows на основе URL-адреса](a-url-based-windows-installer-installation-example.md). Используйте следующий скрипт HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Если щелкнуть ссылку "Установка MySetup", пользователи смогут сохранить или запустить из этого расположения. если пользователь выбирает запуск из этого расположения, Setup.exe обновляет версию установщик Windows на компьютере, при необходимости проверяет цифровую подпись в пакете установщика и устанавливает пакет на своем компьютере.

Это завершает пример.

 

 



