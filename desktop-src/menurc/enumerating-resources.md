---
title: Перечисление ресурсов
description: В этом разделе обсуждаются функции, используемые для получения списков ресурсов.
ms.assetid: 388deaa1-3b04-43fa-aad2-8b52376d570c
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: b978636303f3fc5bcae8c1d854289dde42ae0247
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910267"
---
# <a name="enumerating-resources"></a>Перечисление ресурсов

В некоторых ситуациях может потребоваться обнаружить содержимое ресурсов неизвестного переносимого исполняемого модуля (PE). Windows SDK предоставляет функции перечисления ресурсов, позволяющие приложению получать списки типов ресурсов, имен и языков в указанном модуле.

* Функции [**енумресаурцетипев**](/windows/win32/api/Winbase/nf-winbase-enumresourcetypesw) и [**енумресаурцетипесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcetypesexw) предоставляют список типов ресурсов, найденных в модуле.
* Функции [**енумресаурценамесв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesw) и [**енумресаурценамесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcenamesexw) предоставляют имя каждого ресурса в заданном типе.
* Функции [**енумресаурцелангуажесв**](/windows/win32/api/Winbase/nf-winbase-enumresourcelanguagesw) и [**енумресаурцелангуажесексв**](/windows/win32/api/libloaderapi/nf-libloaderapi-enumresourcelanguagesexw) предоставляют язык для каждого ресурса с заданным именем и типом. 

Эти функции и связанные с ними функции обратного вызова позволяют приложению создать список всех ресурсов в модуле. Этот процесс описан в разделе [Создание списка ресурсов](using-resources.md).

## <a name="-see-also"></a>— см. также

[Msistuff.exe пример приложения](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/sysmgmt/msi/msistuff)
