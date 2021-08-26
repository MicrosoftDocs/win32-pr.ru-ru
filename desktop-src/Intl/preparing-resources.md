---
description: Подготовка ресурсов для приложения MUI поддерживает модели Win32 PE и не Win32 PE.
ms.assetid: e528dac7-c157-42d7-808d-709a4ae84f1e
title: Подготовка ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef40453ca6db40bed1c07bad80f7e21cb7adaa7ea48ae8ee5ce2a2a5c657ba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040674"
---
# <a name="preparing-resources"></a>Подготовка ресурсов

Подготовка ресурсов для приложения MUI поддерживает модели Win32 PE и не Win32 PE. Ресурсы Win32 PE предоставляются в файлах на основе PE, таких как .dll, .exe или файлы .sys. Ресурсы PE, отличные от Win32, предоставляются в настраиваемом модуле по своему выбору.

> [!Note]  
> Настоятельно рекомендуется использовать ресурсы Win32 PE для приложений Win32 MUI, так как эти ресурсы полностью поддерживаются технологией ресурсов MUI. Файлы ресурсов, не относящиеся к Win32 PE, можно найти, вызвав функцию [**жетфилемуипас**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) , как описано в разделе [Поиск ресурсов PE, отличных от Win32](locating-non-win32-pe-resources.md), но приложение должно предоставить собственные функции для поиска и загрузки необходимых ресурсов.

 

В этом разделе рассматриваются следующие вопросы.

-   [Создание файла ресурсов базового языка](creating-the-base-language-resource-file.md)
-   [Использование перенаправления строк реестра](using-registry-string-redirection.md)
-   [Подготовка файла конфигурации ресурса](preparing-a-resource-configuration-file.md)

 

 



