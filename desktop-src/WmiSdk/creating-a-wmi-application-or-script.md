---
description: Любой язык сценариев, например VBScript, который работает с объектами ActiveX, может получать доступ к данным WMI. Приложения могут получать доступ к WMI в C++, используя API COM для WMI или в Visual Basic, используя библиотеку типов Wbemdisp. tlb и API скриптов для WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Создание приложения или скрипта WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703003"
---
# <a name="creating-a-wmi-application-or-script"></a>Создание приложения или скрипта WMI

Любой язык сценариев, например VBScript, который работает с объектами ActiveX, может получать доступ к данным WMI. Приложения могут получать доступ к WMI в C++, используя [API COM для WMI](com-api-for-wmi.md) или в Visual Basic, используя [библиотеку типов](using-the-wmi-scripting-type-library.md) WBEMDISP. tlb и [API скриптов для WMI](scripting-api-for-wmi.md). . Получить данные можно с помощью инструментария WMI, написав сценарий, Active Serverную страницу (ASP) или HTML-приложение (HTA). Можно также использовать Windows PowerShell для получения данных или написания скриптов. Дополнительные сведения см. в статьях [Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) и [Начало работы с помощью Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). TechNet Скриптцентер at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) содержит сотни примеров сценариев. Дополнительные сведения о печати и сетевых ресурсах см. в разделе [Дополнительные сведения](further-information.md).

Следующая процедура описывает подключение к службе WMI и хранилищу данных.

**Подключение к службе WMI и хранилищу данных**

1.  Нахождение службы WMI на определенном компьютере.
2.  Подключитесь к одному или нескольким пространствам имен WMI.

Эти операции отличаются в C++, Visual Basic, платформа .NET Framework языках или при использовании скрипта. Скрипты и Visual Basic приложения должны обращаться к классам, экземпляры которых предоставляются данными существующих поставщиков. Но приложения, написанные на C++, могут сделать больше. Например, приложение, написанное на языке C++, может отправлять события, но сценарий WMI может подписываться только на получение событий.

Поставщик WMI может быть написан только на C++ или с помощью платформа .NET Framework. Дополнительные сведения о создании приложений на C# или Visual Basic .NET см. в разделе [Общие сведения об инструментарии WMI .NET](/previous-versions/bb404655(v=vs.90)).

Дополнительные сведения о создании приложений и скриптов для WMI см. в следующих статьях:

-   [Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md)
-   [Создание скрипта WMI](creating-a-wmi-script.md)
-   [Создание управляемого клиента WMI](creating-a-managed-wmi-client.md)

Для выполнения большинства задач используйте предустановленные [классы WMI](wmi-classes.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование инструментария WMI](using-wmi.md)
</dt> </dl>

 

 
