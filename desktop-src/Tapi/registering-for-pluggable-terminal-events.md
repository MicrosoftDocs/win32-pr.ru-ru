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
# <a name="registering-for-pluggable-terminal-events"></a>Регистрация для подключаемых событий терминала

Процесс регистрации событий происходит, когда терминал выбирается потоком. В реализации метода [**селекттерминал**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) в приложении терминала можно использовать интерфейс [**иттерминал**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) терминала, который был подключен к потоку, и вызвать метод **QueryInterface** , чтобы найти [**итплуггаблетерминалевентсинкрегистратион**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration).

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

Если вызов **QueryInterface** завершился с ошибкой, мы можем вызвать метод [**регистерсинк**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) . Для этой цели следует создать объект, реализующий интерфейс [**итплуггаблетерминалевентсинк**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) . Мы передаем этот интерфейс в качестве параметра метода **регистерсинк** .

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

В терминале, который реализует вызов [**итплуггаблетерминалевентсинкрегистратион**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) , будет сохранен интерфейс. Указатель будет использоваться, когда терминал запустит событие.

Регистрация приемника событий может быть отменена с помощью [**унрегистерсинк**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink).

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
