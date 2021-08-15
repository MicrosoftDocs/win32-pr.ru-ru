---
description: В следующем примере кода демонстрируется обработка новых уведомлений о вызовах, например поиск или создание соответствующих терминалов для подготовки к просмотру мультимедиа.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Получение вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e4ce02ec11a1373d16b9b9ebd0fba29313b1d532175894c6fd1b12a38e2bf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060472"
---
# <a name="receive-a-call"></a>Получение вызова

В следующем примере кода демонстрируется обработка новых уведомлений о вызовах, например поиск или создание соответствующих терминалов для подготовки к просмотру мультимедиа. Этот пример представляет собой часть оператора switch, которую приложение должно реализовать для обработки событий. Сам код может содержаться в реализации [**иттапиевентнотификатион:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), или метод **события** может поместить сообщение в рабочий поток, содержащий параметр.

Перед использованием этого примера кода необходимо выполнить операции в оснастке [инициализации TAPI](initialize-tapi.md), [выбрать адрес](select-an-address.md)и [зарегистрировать события](register-events.md).

Кроме того, необходимо выполнить операции, показанные в окне [Выбор терминала](select-a-terminal.md) после получения указателей интерфейса [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) и [**итаддресс**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) .

> [!Note]  
> В этом примере отсутствует проверка ошибок и выпуски, соответствующие рабочему коду.

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[События](events.md)
</dt> <dt>

[**иттапиевентнотификатион**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**ИТТАПИ:: Регистеркаллнотификатионс**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**иткаллнотификатионевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**иткаллинфо**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**иттерминалсуппорт**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
