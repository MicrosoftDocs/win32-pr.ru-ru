---
description: Скрипты могут обращаться ко всем классам WMI для аппаратных и программных объектов.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Создание сценариев для доступа к инструментарию WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263814"
---
# <a name="scripting-access-to-wmi"></a>Создание сценариев для доступа к инструментарию WMI

Скрипты могут обращаться ко всем классам WMI для аппаратных и программных объектов. Сценарии сервера сценариев Windows (WSH) могут выполнять операции с объектами файловой системы, управлять сетевыми принтерами или изменять переменные среды. Вы можете найти разнообразные задачи администратора и краткое руководство по их выполнению в инструментарии WMI в [задачах WMI для сценариев и приложений](wmi-tasks-for-scripts-and-applications.md). Дополнительные сведения и примеры см. в [репозитории сценариев](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)TechNet скриптцентер.

Если вы не знакомы со сценариями или с помощью сценариев для WMI, см. раздел [Начало работы](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)TechNet скриптцентер.

С помощью [API скриптов для WMI](scripting-api-for-wmi.md)можно разрабатывать быстрые, простые сценарии или сложные приложения. Создание сценариев предоставляет такую же возможность для получения информации или настройки большинства объектов на предприятии, как и с помощью приложения C++ или C#. Дополнительные сведения см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Невозможно создать [*поставщик WMI*](gloss-p.md) в скрипте. Дополнительные сведения см. [в разделе Предоставление данных инструментарию WMI](providing-data-to-wmi.md).

Сценарии WMI могут быть написаны на любом языке сценариев, который может взаимодействовать с объектами ActiveX.

Windows PowerShell предоставляет простую среду для администрирования WMI и создания сценариев. Дополнительные сведения об PowerShell см. [в разделе Начало работы with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).

Сценарии интерфейсов служб Active Directory (ADSI) предоставляют доступ к объектам домен Active Directory служб (AD DS). Скрипты WSH и ADSI обращаются к объектам и разрешают процедуры, недоступные через пакетные файлы.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> <dt>

[API сценариев для инструментария WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
