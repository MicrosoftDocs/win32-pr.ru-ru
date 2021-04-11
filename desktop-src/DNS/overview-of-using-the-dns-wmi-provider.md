---
title: Общие сведения об использовании поставщика WMI для DNS
description: Следующие общие шаги помогут вам приступить к созданию собственного сценария или программы, использующей поставщик WMI для DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068258"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Общие сведения об использовании поставщика WMI для DNS

Следующие общие шаги помогут вам приступить к созданию собственного сценария или программы, использующей поставщик WMI для DNS.

**Создание скрипта или программы с помощью поставщика WMI DNS**

1.  Подключитесь к поставщику WMI DNS.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > Пространство имен для поставщика DNS WMI всегда будет иметь значение root \\ микрософтднс.

     

2.  Получение экземпляра DNS-сервера.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  В зависимости от действия типа, которое вы хотите выполнить, получите зону DNS или экземпляр записи.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Выполните требуемые действия:
    -   Выполнение метода
    -   Отображение свойства
    -   Изменение свойства (требуется доступ на чтение и запись)

 

 




