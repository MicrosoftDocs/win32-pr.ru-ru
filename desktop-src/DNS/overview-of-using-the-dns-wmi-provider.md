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
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="2e553-103">Общие сведения об использовании поставщика WMI для DNS</span><span class="sxs-lookup"><span data-stu-id="2e553-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="2e553-104">Следующие общие шаги помогут вам приступить к созданию собственного сценария или программы, использующей поставщик WMI для DNS.</span><span class="sxs-lookup"><span data-stu-id="2e553-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="2e553-105">**Создание скрипта или программы с помощью поставщика WMI DNS**</span><span class="sxs-lookup"><span data-stu-id="2e553-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="2e553-106">Подключитесь к поставщику WMI DNS.</span><span class="sxs-lookup"><span data-stu-id="2e553-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="2e553-107">Пространство имен для поставщика DNS WMI всегда будет иметь значение root \\ микрософтднс.</span><span class="sxs-lookup"><span data-stu-id="2e553-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="2e553-108">Получение экземпляра DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="2e553-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="2e553-109">В зависимости от действия типа, которое вы хотите выполнить, получите зону DNS или экземпляр записи.</span><span class="sxs-lookup"><span data-stu-id="2e553-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="2e553-110">Выполните требуемые действия:</span><span class="sxs-lookup"><span data-stu-id="2e553-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="2e553-111">Выполнение метода</span><span class="sxs-lookup"><span data-stu-id="2e553-111">Execute a method</span></span>
    -   <span data-ttu-id="2e553-112">Отображение свойства</span><span class="sxs-lookup"><span data-stu-id="2e553-112">Display a property</span></span>
    -   <span data-ttu-id="2e553-113">Изменение свойства (требуется доступ на чтение и запись)</span><span class="sxs-lookup"><span data-stu-id="2e553-113">Modify a property (must have Read/Write access)</span></span>

 

 




