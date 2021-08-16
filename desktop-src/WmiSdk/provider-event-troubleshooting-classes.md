---
description: В следующей таблице перечислены классы для устранения неполадок событий поставщика WMI. Каждый класс связан с событием поставщика WMI, к которому оно привязано.
ms.assetid: 5acfc8f4-9b3b-4ff4-a8ed-7378334a8ddb
ms.tgt_platform: multiple
title: Классы устранения неполадок событий поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6530543abd63d656c13b77fdf5138b64079886fd7e1906dd9a8692f705659343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131016"
---
# <a name="provider-event-troubleshooting-classes"></a>Классы устранения неполадок событий поставщика

В следующей таблице перечислены классы для устранения неполадок событий поставщика WMI. Каждый класс связан с событием поставщика WMI, к которому оно привязано.



| Класс                                                                                                                            | Описание                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Сообщение о событияе \_ AccessCheck MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post)                                      | Экземпляр класса событий, созданный сразу после завершения реализации поставщика [**ивбемевентпровидерсекурити:: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck).   |
| [**MSFT \_ события \_ AccessCheck, \_ предварительно**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre)                                        | Экземпляр класса событий, созданный непосредственно перед вызовом реализации поставщика [**ивбемевентпровидерсекурити:: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck).          |
| [**\_Сообщение MSFT события \_ канцелкуери \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-cancelquery-post)                                      | Экземпляр класса событий, созданный сразу после завершения реализации поставщика [**ивбемевентпровидеркуерисинк:: канцелкуери**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery). |
| [**MSFT \_ события \_ канцелкуери \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-cancelquery-pre)                                        | Экземпляр класса событий, созданный непосредственно перед вызовом реализации поставщика [**ивбемевентпровидеркуерисинк:: канцелкуери**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery).        |
| [**MSFT \_ события \_ комсерверлоадоператионевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-comserverloadoperationevent)                 | Экземпляр класса событий, созданный для активации экземпляра COM-сервера.                                                                                                                               |
| [**MSFT \_ события \_ комсерверлоадоператионфаилуривент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-comserverloadoperationfailureevent)   | Экземпляр класса событий, созданный для сбоя активации экземпляра COM-сервера.                                                                                                                       |
| [**\_Сообщение MSFT события \_ креатеклассенумасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createclassenumasyncevent-post)          | Экземпляр класса событий, созданный сразу после завершения реализации метода [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)поставщика.           |
| [**MSFT \_ события \_ креатеклассенумасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createclassenumasyncevent-pre)            | Экземпляр класса событий, созданный непосредственно перед вызовом реализации [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)поставщика.                  |
| [**\_Сообщение MSFT события \_ креатеинстанцеенумасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post)    | Экземпляр класса событий, созданный сразу после завершения реализации метода [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)поставщика.     |
| [**MSFT \_ события \_ креатеинстанцеенумасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-pre)      | Экземпляр класса событий, созданный непосредственно перед вызовом реализации [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)поставщика.            |
| [**\_Сообщение MSFT события \_ делетеклассасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteclassasyncevent-post)                  | Экземпляр класса событий, созданный сразу после завершения реализации [**IWbemServices::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync).                   |
| [**MSFT \_ события \_ делетеклассасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteclassasyncevent-pre)                    | Экземпляр класса событий, созданный непосредственно перед вызовом реализации IWbemServices для поставщика [**::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync).                          |
| [**\_Сообщение MSFT события \_ делетеинстанцеасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteinstanceasyncevent-post)            | Экземпляр класса событий, созданный сразу после завершения реализации [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).             |
| [**MSFT \_ события \_ делетеинстанцеасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-deleteinstanceasyncevent-pre)              | Экземпляр класса событий, созданный непосредственно перед вызовом реализации IWbemServices для поставщика [**::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).                    |
| [**\_Сообщение MSFT события \_ ексекмесодасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)                    | Экземпляр класса событий, созданный сразу после завершения реализации метода [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)поставщика.                     |
| [**MSFT \_ события \_ ексекмесодасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)                      | Экземпляр класса событий, созданный непосредственно перед вызовом реализации [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)поставщика.                            |
| [**\_Сообщение MSFT события \_ ексеккуерясинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execqueryasyncevent-post)                      | Экземпляр класса событий, созданный сразу после завершения реализации метода [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)поставщика.                       |
| [**MSFT \_ события \_ ексеккуерясинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execqueryasyncevent-pre)                        | Экземпляр класса событий, созданный непосредственно перед вызовом реализации [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)поставщика.                              |
| [**\_Сообщение MSFT события \_ жетобжектасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-getobjectasyncevent-post)                      | Экземпляр класса событий, созданный сразу после завершения реализации метода [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)поставщика.                       |
| [**MSFT \_ события \_ жетобжектасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-getobjectasyncevent-pre)                        | Экземпляр класса событий, созданный непосредственно перед вызовом реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)поставщика.                              |
| [**MSFT \_ события \_ инитиализатионоператионевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-initializationoperationevent)               | Экземпляр класса событий, созданный для успешной инициализации экземпляра сервера поставщика.                                                                                                    |
| [**MSFT \_ события \_ инитиализатионоператионфаилуривент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-initializationoperationfailureevent) | Экземпляр класса событий, созданный для неудачной инициализации экземпляра сервера поставщика.                                                                                                        |
| [**MSFT \_ события \_ лоадоператионевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationevent)                                   | Экземпляр класса событий создан или прошел активацию и инициализацию записи кэша поставщика.                                                                                          |
| [**MSFT \_ события \_ лоадоператионфаилуривент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent)                     | Экземпляр класса событий, созданный для неудачной активации и инициализации записи кэша поставщика.                                                                                             |
| [**\_Сообщение MSFT события \_ невкуери \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-newquery-post)                                            | Экземпляр класса событий, созданный сразу после завершения реализации поставщика [**ивбемевентпровидеркуерисинк:: невкуери**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery).       |
| [**MSFT \_ события \_ невкуери \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-newquery-pre)                                              | Экземпляр класса событий, созданный непосредственно перед вызовом реализации поставщика [**ивбемевентпровидеркуерисинк:: невкуери**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery).              |
| [**MSFT \_ события \_ оператионевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent)                                           | Базовый класс для классов событий устранения неполадок поставщика WMI.                                                                                                                                       |
| [**\_Сообщение MSFT события \_ оператионевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent-post)                                | Базовый класс для устранения неполадок событий после завершения реализации поставщика.                                                                                                           |
| [**MSFT \_ события \_ оператионевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent-pre)                                  | Базовый класс для устранения неполадок событий до вызова реализации поставщика.                                                                                                                  |
| [**\_Сообщение MSFT события \_ провидивентс \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-provideevents-post)                                  | Экземпляр класса событий, созданный сразу после завершения реализации поставщика [**ивбемевентпровидер::P ровидивентс**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents).               |
| [**MSFT \_ события \_ провидивентс \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-provideevents-pre)                                    | Экземпляр класса событий, созданный непосредственно перед вызовом реализации поставщика [**ивбемевентпровидер::P ровидивентс**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents).                      |
| [**\_Сообщение MSFT события \_ путклассасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putclassasyncevent-post)                        | Экземпляр класса событий, созданный сразу после завершения реализации [**IWbemServices::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync).                         |
| [**MSFT \_ события \_ путклассасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putclassasyncevent-pre)                          | Экземпляр класса событий, созданный непосредственно перед вызовом реализации IWbemServices для поставщика [**::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync).                                |
| [**\_Сообщение MSFT события \_ путинстанцеасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putinstanceasyncevent-post)                  | Экземпляр класса событий, созданный сразу после завершения реализации [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).                   |
| [**MSFT \_ события \_ путинстанцеасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-putinstanceasyncevent-pre)                    | Экземпляр класса событий, созданный непосредственно перед вызовом реализации IWbemServices для поставщика [**::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).                          |
| [**MSFT \_ события \_ унлоадоператионевент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-unloadoperationevent)                               | Экземпляр класса событий, созданный для удаления записи кэша поставщика.                                                                                                                          |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md)
</dt> <dt>

Устранение неполадок инструментария WMI
</dt> <dt>

[Получение события WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
