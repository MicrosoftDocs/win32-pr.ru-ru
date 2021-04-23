---
title: Реализация виртуальных каналов с использованием скриптов с помощью веб-подключение к удаленному рабочему столу
description: Примеры кода, демонстрирующие шаги для реализации виртуальных каналов с помощью сценариев с веб-подключение к удаленному рабочему столу.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777753"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="fc0a2-103">Реализация виртуальных каналов с использованием скриптов с помощью веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="fc0a2-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="fc0a2-104">В приведенной ниже процедуре и примерах кода показаны шаги для реализации сценариев с использованием скриптов с веб-подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="fc0a2-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="fc0a2-105">Примеры написаны на Visual Basic Scripting Edition и предполагают, что удаленный рабочий стол элемент управления ActiveX называется "Мсрдпклиент".</span><span class="sxs-lookup"><span data-stu-id="fc0a2-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="fc0a2-106">**Создание и развертывание виртуальных каналов, поддерживающих сценарии**</span><span class="sxs-lookup"><span data-stu-id="fc0a2-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="fc0a2-107">Разверните серверную часть приложения и убедитесь, что оно выполняется на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="fc0a2-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="fc0a2-108">Сведения о развертывании приложений виртуальных каналов на сервере см. в разделе [серверное приложение виртуальных каналов](virtual-channel-server-application.md).</span><span class="sxs-lookup"><span data-stu-id="fc0a2-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="fc0a2-109">В клиентском скрипте вызовите [**имстскакс:: креатевиртуалчаннелс**](imstscax-createvirtualchannels.md), передав строку, содержащую список имен виртуальных каналов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="fc0a2-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="fc0a2-110">Сведения об ограничениях именования виртуальных каналов см. в разделе [Регистрация клиента для виртуального канала](virtual-channel-client-registration.md).</span><span class="sxs-lookup"><span data-stu-id="fc0a2-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="fc0a2-111">Вызовите [**имстскакс:: Connect**](imstscax-connect.md) , чтобы создать подключение к службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fc0a2-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="fc0a2-112">Используйте метод [**имстскакс:: сендонвиртуалчаннел**](imstscax-sendonvirtualchannel.md) для отправки данных на сервер, передав строку, содержащую имя виртуального канала, и вторую строку, содержащую данные для передачи.</span><span class="sxs-lookup"><span data-stu-id="fc0a2-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="fc0a2-113">Получение данных с сервера в событии [**имстскаксевентс:: ончаннелрецеиведдата**](imstscaxevents-onchannelreceiveddata.md) .</span><span class="sxs-lookup"><span data-stu-id="fc0a2-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




