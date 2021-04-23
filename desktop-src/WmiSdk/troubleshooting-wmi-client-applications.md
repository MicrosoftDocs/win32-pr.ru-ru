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
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265595"
---
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="85dc5-103">Устранение неполадок клиентских приложений WMI</span><span class="sxs-lookup"><span data-stu-id="85dc5-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="85dc5-104">Инструментарий WMI содержит набор классов для [устранения неполадок](wmi-troubleshooting-classes.md) клиентских приложений, использующих поставщики WMI.</span><span class="sxs-lookup"><span data-stu-id="85dc5-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="85dc5-105">Классы событий устранения неполадок связаны с классами событий WMI, что позволяет отслеживать выполнение приложения с помощью журнала записанных событий устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="85dc5-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="85dc5-106">В следующем списке приведены примеры устранения неполадок классов событий.</span><span class="sxs-lookup"><span data-stu-id="85dc5-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="85dc5-107">**MSFT \_ события \_ ексекмесодасинцевент \_ до**</span><span class="sxs-lookup"><span data-stu-id="85dc5-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="85dc5-108">Вызывается перед тем, как WMI вызывает [**IWbemServices:: ексекмесодасинк ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) в поставщике.</span><span class="sxs-lookup"><span data-stu-id="85dc5-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="85dc5-109">**\_Сообщение MSFT события \_ ексекмесодасинцевент \_**</span><span class="sxs-lookup"><span data-stu-id="85dc5-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="85dc5-110">Вызывается после того, как WMI вызывает [**IWbemServices:: ексекмесодасинк ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) в поставщике.</span><span class="sxs-lookup"><span data-stu-id="85dc5-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="85dc5-111">В следующей процедуре показано, как устранить неполадки при выполнении приложения.</span><span class="sxs-lookup"><span data-stu-id="85dc5-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="85dc5-112">**Настройка устранения неполадок WMI**</span><span class="sxs-lookup"><span data-stu-id="85dc5-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="85dc5-113">Создайте и Скомпилируйте MOF-файл для использования объекта-получателя событий ведения журнала WMI.</span><span class="sxs-lookup"><span data-stu-id="85dc5-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="85dc5-114">Запустите клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="85dc5-114">Run your client application.</span></span>
3.  <span data-ttu-id="85dc5-115">Просмотрите файл журнала устранения неполадок для всех операций поставщика и событий сбоя, а также проанализируйте журнал, чтобы диагностировать возникшие проблемы клиента.</span><span class="sxs-lookup"><span data-stu-id="85dc5-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="85dc5-116">Другим способом устранения неполадок является просмотр списка поставщиков, находящихся в кэше компьютера, путем перечисления [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) в **корневом пространстве имен \\ CIMV2** .</span><span class="sxs-lookup"><span data-stu-id="85dc5-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="85dc5-117">В этом классе есть методы, позволяющие загружать и выгружать поставщики в целях отладки или настройки.</span><span class="sxs-lookup"><span data-stu-id="85dc5-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="85dc5-118">В следующем примере кода потребитель событий ведения журнала WMI используется для сбора всех событий родительского класса событий, тем самым записывая все события операции поставщика.</span><span class="sxs-lookup"><span data-stu-id="85dc5-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

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

<span data-ttu-id="85dc5-119">Если сообщения об ошибках указывают на сбой загрузки поставщика, используйте [**MSFT \_ события \_ лоадоператионфаилуривент**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) , чтобы определить, какой поставщик вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="85dc5-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85dc5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="85dc5-120">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="85dc5-121">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="85dc5-121">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="85dc5-122">Классы устранения неполадок WMI</span><span class="sxs-lookup"><span data-stu-id="85dc5-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
