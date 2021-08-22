---
title: Перечисление ресурсов
description: В этом разделе обсуждаются функции, используемые для получения списков ресурсов.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 6d3fbe60e3013fbeabdb21d74999040b51c42be2a1bb4521cda28a976bfe7aa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034342"
---
# <a name="enumerating-resources"></a>Перечисление ресурсов

В некоторых ситуациях может потребоваться обнаружить содержимое ресурсов неизвестного переносимого исполняемого модуля (PE). Windows SDK предоставляет функции перечисления ресурсов, позволяющие приложению получать списки типов ресурсов, имен и языков в указанном модуле.

* Функции [**енумресаурцетипев**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) и [**енумресаурцетипесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) предоставляют список типов ресурсов, найденных в модуле.
* Функции [**енумресаурценамесв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) и [**енумресаурценамесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) предоставляют имя каждого ресурса в заданном типе.
* Функции [**енумресаурцелангуажесв**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) и [**енумресаурцелангуажесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) предоставляют язык для каждого ресурса с заданным именем и типом. 

Эти функции и связанные с ними функции обратного вызова позволяют приложению создать список всех ресурсов в модуле. Этот процесс описан в разделе [Создание списка ресурсов](using-resources.md).

## <a name="-see-also"></a>— см. также

[Msistuff.exe пример приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
