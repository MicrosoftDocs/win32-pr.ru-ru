---
description: любой язык сценариев, например VBScript, который работает с ActiveX объектами, может получать доступ к данным WMI. приложения могут получать доступ к WMI в C++, используя API COM для WMI или в Visual Basic, используя библиотеку типов Wbemdisp. tlb и API скриптов для WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Создание приложения или скрипта WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddde26b2a8495126b4aa26c132adb49860627230d698431df5d713e653f1d874
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412134"
---
# <a name="creating-a-wmi-application-or-script"></a>Создание приложения или скрипта WMI

любой язык сценариев, например VBScript, который работает с ActiveX объектами, может получать доступ к данным WMI. приложения могут получать доступ к WMI в C++, используя [API COM для WMI](com-api-for-wmi.md) или в Visual Basic, используя [библиотеку типов](using-the-wmi-scripting-type-library.md) Wbemdisp. tlb и [API скриптов для WMI](scripting-api-for-wmi.md). . Получить данные можно с помощью инструментария WMI, написав сценарий, Active Serverную страницу (ASP) или HTML-приложение (HTA). можно также использовать Windows PowerShell для получения данных или создания скриптов. Дополнительные сведения см. [в разделе Создание скриптов в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) и [начало работы с помощью Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true). TechNet Скриптцентер at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) содержит сотни примеров сценариев. Дополнительные сведения о печати и сетевых ресурсах см. в разделе [Дополнительные сведения](further-information.md).

Следующая процедура описывает подключение к службе WMI и хранилищу данных.

**Подключение к службе WMI и хранилищу данных**

1.  Нахождение службы WMI на определенном компьютере.
2.  Подключение в одно или несколько пространств имен WMI.

эти операции отличаются в C++, Visual Basic, платформа .NET Framework языках или при использовании скрипта. скрипты и Visual Basic приложения должны обращаться к классам, экземпляры которых предоставляются данными существующих поставщиков. Но приложения, написанные на C++, могут сделать больше. Например, приложение, написанное на языке C++, может отправлять события, но сценарий WMI может подписываться только на получение событий.

поставщик WMI может быть написан только на C++ или с помощью платформа .NET Framework. дополнительные сведения о создании приложений на C# или Visual Basic .net см. в разделе [общие сведения об инструментарии WMI .net](/previous-versions/bb404655(v=vs.90)).

Дополнительные сведения о создании приложений и скриптов для WMI см. в следующих статьях:

-   [Создание приложения WMI с помощью C++](creating-a-wmi-application-using-c-.md)
-   [Создание скрипта WMI](creating-a-wmi-script.md)
-   [Создание управляемого клиента WMI](creating-a-managed-wmi-client.md)

Для выполнения большинства задач используйте предустановленные [классы WMI](wmi-classes.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование инструментария WMI](using-wmi.md)
</dt> </dl>

 

 
