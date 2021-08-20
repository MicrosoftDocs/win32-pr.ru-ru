---
description: Инструментарий WMI содержит набор классов для устранения неполадок клиентских приложений, использующих поставщики WMI.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Устранение неполадок клиентских приложений WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7fb9eb8c438faab8915691ee2c9c8a4c77d247c6802f8f114683a79d2833bd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050032"
---
# <a name="troubleshooting-wmi-client-applications"></a>Устранение неполадок клиентских приложений WMI

Инструментарий WMI содержит набор классов для [устранения неполадок](wmi-troubleshooting-classes.md) клиентских приложений, использующих поставщики WMI. Классы событий устранения неполадок связаны с классами событий WMI, что позволяет отслеживать выполнение приложения с помощью журнала записанных событий устранения неполадок.

В следующем списке приведены примеры устранения неполадок классов событий.

-   [**MSFT \_ события \_ ексекмесодасинцевент \_ до**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Вызывается перед тем, как WMI вызывает [**IWbemServices:: ексекмесодасинк ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) в поставщике.

-   [**\_Сообщение MSFT события \_ ексекмесодасинцевент \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Вызывается после того, как WMI вызывает [**IWbemServices:: ексекмесодасинк ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) в поставщике.

В следующей процедуре показано, как устранить неполадки при выполнении приложения.

**Настройка устранения неполадок WMI**

1.  Создайте и Скомпилируйте MOF-файл для использования объекта-получателя событий ведения журнала WMI.
2.  Запустите клиентское приложение.
3.  Просмотрите файл журнала устранения неполадок для всех операций поставщика и событий сбоя, а также проанализируйте журнал, чтобы диагностировать возникшие проблемы клиента.

Другим способом устранения неполадок является просмотр списка поставщиков, находящихся в кэше компьютера, путем перечисления [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) в **корневом пространстве имен \\ CIMV2** . В этом классе есть методы, позволяющие загружать и выгружать поставщики в целях отладки или настройки.

В следующем примере кода потребитель событий ведения журнала WMI используется для сбора всех событий родительского класса событий, тем самым записывая все события операции поставщика.

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

Если сообщения об ошибках указывают на сбой загрузки поставщика, используйте [**MSFT \_ события \_ лоадоператионфаилуривент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) , чтобы определить, какой поставщик вызвал ошибку.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Устранение неполадок WMI](wmi-troubleshooting.md)
</dt> <dt>

[Классы устранения неполадок WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
