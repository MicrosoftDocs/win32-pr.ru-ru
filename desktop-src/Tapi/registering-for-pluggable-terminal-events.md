---
description: Процесс регистрации событий происходит, когда терминал выбирается потоком.
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: Регистрация для подключаемых событий терминала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d42bf75cfd0d7e6bd4d8a2520335c374cce28c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913815"
---
# <a name="registering-for-pluggable-terminal-events"></a><span data-ttu-id="96d42-103">Регистрация для подключаемых событий терминала</span><span class="sxs-lookup"><span data-stu-id="96d42-103">Registering for Pluggable Terminal Events</span></span>

<span data-ttu-id="96d42-104">Процесс регистрации событий происходит, когда терминал выбирается потоком.</span><span class="sxs-lookup"><span data-stu-id="96d42-104">The event registration process take place when the terminal is selected by a stream.</span></span> <span data-ttu-id="96d42-105">В реализации метода [**селекттерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) в приложении терминала можно использовать интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) терминала, который был подключен к потоку, и вызвать метод **QueryInterface** , чтобы найти [**итплуггаблетерминалевентсинкрегистратион**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span><span class="sxs-lookup"><span data-stu-id="96d42-105">In the terminal application's implementation of the [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) method, we can use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of the terminal that was attached to the stream, and call **QueryInterface** to find [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).</span></span>

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

<span data-ttu-id="96d42-106">Если вызов **QueryInterface** завершился с ошибкой, мы можем вызвать метод [**регистерсинк**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) .</span><span class="sxs-lookup"><span data-stu-id="96d42-106">If the **QueryInterface** call succeeds, we can call the [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) method.</span></span> <span data-ttu-id="96d42-107">Для этой цели следует создать объект, реализующий интерфейс [**итплуггаблетерминалевентсинк**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) .</span><span class="sxs-lookup"><span data-stu-id="96d42-107">For this purpose, we should create an object that implements the [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) interface.</span></span> <span data-ttu-id="96d42-108">Мы передаем этот интерфейс в качестве параметра метода **регистерсинк** .</span><span class="sxs-lookup"><span data-stu-id="96d42-108">We pass this interface as a parameter of the **RegisterSink** method.</span></span>

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

<span data-ttu-id="96d42-109">В терминале, который реализует вызов [**итплуггаблетерминалевентсинкрегистратион**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) , будет сохранен интерфейс.</span><span class="sxs-lookup"><span data-stu-id="96d42-109">The terminal that implements the [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) call will store the interface.</span></span> <span data-ttu-id="96d42-110">Указатель будет использоваться, когда терминал запустит событие.</span><span class="sxs-lookup"><span data-stu-id="96d42-110">The pointer will be used when the terminal will fire an event.</span></span>

<span data-ttu-id="96d42-111">Регистрация приемника событий может быть отменена с помощью [**унрегистерсинк**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span><span class="sxs-lookup"><span data-stu-id="96d42-111">The event sink can be unregistered using [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).</span></span>

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
