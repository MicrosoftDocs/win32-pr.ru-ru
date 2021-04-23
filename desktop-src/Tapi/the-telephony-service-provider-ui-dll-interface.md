---
description: В Microsoft телефонии поставщики услуг телефонии выполняются в отдельном процессе из приложений телефонии.
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: Интерфейс библиотеки DLL интерфейса поставщика услуг телефонии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673696"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a><span data-ttu-id="99017-103">Интерфейс библиотеки DLL интерфейса поставщика услуг телефонии</span><span class="sxs-lookup"><span data-stu-id="99017-103">The Telephony Service Provider UI DLL Interface</span></span>

<span data-ttu-id="99017-104">В Microsoft телефонии поставщики услуг телефонии выполняются в отдельном процессе из приложений телефонии.</span><span class="sxs-lookup"><span data-stu-id="99017-104">In Microsoft Telephony, telephony service providers execute in a separate process from telephony applications.</span></span> <span data-ttu-id="99017-105">Поставщики услуг взаимодействуют с ТАПИСРВ через интерфейс поставщика услуг телефонии (ТСПИ) и выполняются в процессе. интерфейс приложений для TAPI, которые загружаются в контексте приложения.</span><span class="sxs-lookup"><span data-stu-id="99017-105">Service providers communicate with TAPISRV through the Telephony service provider interface (TSPI) and execute in its process; applications interface to TAPI, which are loaded in the application context.</span></span>

<span data-ttu-id="99017-106">Компоненты TAPI используют различные механизмы межпроцессного взаимодействия для передачи запросов функций и сообщений между приложениями и поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="99017-106">The components of TAPI use various interprocess communications mechanisms to convey function requests and messages between applications and service providers.</span></span> <span data-ttu-id="99017-107">Приложения и поставщики служб могут выполняться не только в отдельных процессах, но и на совершенно отдельных системах.</span><span class="sxs-lookup"><span data-stu-id="99017-107">The applications and the service providers may be executing not only in separate processes, but on completely separate systems.</span></span> <span data-ttu-id="99017-108">Поэтому поставщики услуг не могут отображать диалоговые окна в процессе или даже на компьютере, на котором они выполняются; Пользовательский интерфейс должен вызываться в контексте приложения на компьютере, где выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="99017-108">Service providers therefore cannot display dialog boxes in the process or even on the computer on which they are executing; UI must be invoked from within the application context, on the computer on which the application is executing.</span></span>

<span data-ttu-id="99017-109">В этом разделе определяется механизм, по которому функции пользовательского интерфейса поставщика услуг загружаются и вызываются в контексте приложения.</span><span class="sxs-lookup"><span data-stu-id="99017-109">This section defines the mechanism by which service provider UI functions are loaded and invoked within the application context.</span></span> <span data-ttu-id="99017-110">Механизм также определяется тем, какие поставщики служб могут нормально открывать диалоговые окна в контексте приложения, если они не ожидались приложением в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99017-110">A mechanism is also defined by which service providers can spontaneously open dialog boxes in the application context when they would not otherwise be expected by the application.</span></span> <span data-ttu-id="99017-111">В качестве примера можно привести диалоговое окно " **разговор и разрыв соединения** ", которое отображается поставщиком службы модема данных, когда модем используется в качестве номеронабирателя для интерактивных голосовых вызовов, и пользователь должен сообщить о том, что нужно выбрать телефон и сообщить поставщику услуг о необходимости подключения модема.</span><span class="sxs-lookup"><span data-stu-id="99017-111">An example of this latter case would be the **Talk/Hangup** dialog box that is displayed by a data modem service provider when the modem is being used as a dialer for interactive voice calls, and the user must be told to pick up the phone and inform the service provider when to place the modem onhook.</span></span>

 

 



