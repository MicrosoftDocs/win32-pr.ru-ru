---
description: Подготовка ресурсов для приложения MUI поддерживает модели Win32 PE и не Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Подготовка ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ca7655535318fa7a385993e6a55f9e7b6110ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684241"
---
# <a name="preparing-resources"></a>Подготовка ресурсов

Подготовка ресурсов для приложения MUI поддерживает модели Win32 PE и не Win32 PE. Ресурсы Win32 PE предоставляются в файлах на основе PE, таких как DLL, exe или sys-файлы. Ресурсы PE, отличные от Win32, предоставляются в настраиваемом модуле по своему выбору.

> [!Note]  
> Настоятельно рекомендуется использовать ресурсы Win32 PE для приложений Win32 MUI, так как эти ресурсы полностью поддерживаются технологией ресурсов MUI. Файлы ресурсов, не относящиеся к Win32 PE, можно найти, вызвав функцию [**жетфилемуипас**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , как описано в разделе [Поиск ресурсов PE, отличных от Win32](locating-non-win32-pe-resources.md), но приложение должно предоставить собственные функции для поиска и загрузки необходимых ресурсов.

 

В этом разделе рассматриваются следующие вопросы.

-   [Создание файла ресурсов базового языка](creating-the-base-language-resource-file.md)
-   [Использование перенаправления строк реестра](using-registry-string-redirection.md)
-   [Подготовка файла конфигурации ресурса](preparing-a-resource-configuration-file.md)

 

 



