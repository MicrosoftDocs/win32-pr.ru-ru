---
description: Microsoft Network Monitor 3 (Netmon) — анализатор пакетов, используемый для проверки сетевого трафика.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Загрузка Netmon и примеров фильтров DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6f92f2680807101a3c82664f4b0b3ae5a877f0d9f5797da9c9c0b6ea2b158
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030224"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a>Загрузка Netmon и примеров фильтров DPWS

Microsoft Network Monitor 3 (Netmon) — анализатор пакетов, используемый для проверки сетевого трафика. сетевой монитор должен быть скачан перед действиями по устранению неполадок, описанных в статье [проверка трассировки сети для протокола UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) и [проверка трассировки сети для метаданных HTTP Exchange](inspecting-network-traces-for-http-metadata-exchange.md) можно проследить. После загрузки netmon можно использовать фильтры DPWS, помогающие изолировать интересующий вас трафик.

## <a name="downloading-netmon"></a>Загрузка Netmon

Чтобы скачать NetMon, перейдите по адресу [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) и следуйте инструкциям. Дополнительные сведения о netmon см. в разделе «сведения о сетевой монитор 3,0» в базе знаний справки и поддержки по адресу [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

## <a name="sample-dpws-filters"></a>Примеры фильтров DPWS

Иногда WS-Discovery и устранение неполадок в обмене метаданными должны происходить в занятой сети. Примеры фильтров можно использовать для ограничения выходных данных NetMon на интересующий вас трафик. Дополнительные сведения об использовании фильтров Netmon см. в разделе [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .

В следующем примере показан фильтр, ограничивающий вывод для всех широковещательных WS-Discovery трафика.

> [!Note]  
> Этот фильтр не записывает трафик из стеков, которые не отвечают на многоадресные WS-Discovery сообщениям, источником которых является порт 3702. Если такой стек используется, то этот образец фильтра необходимо изменить перед использованием.

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

В следующем примере показан фильтр, ограничивающий вывод HTTP-сообщений, отправляемых в стеки WSDAPI на порте по умолчанию.

> [!Note]  
> Службы могут отсылать соответствующие HTTP-сообщения от портов, отличных от 5357. Если трафик от других портов представляет интерес, этот фильтр необходимо изменить перед использованием.

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

В следующем примере показан фильтр, который ограничивает выходные данные трафиком многоадресной рассылки IPv4.

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

В следующем примере показан фильтр, который ограничивает вывод трафика многоадресной рассылки IPv6.

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

Некоторые фильтры можно комбинировать для дальнейшего ограничения результатов. В следующем примере показан фильтр, ограничивающий вывод на многоадресный трафик IPv4 WS-Discovery.

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

При использовании этих фильтров соответствующий трафик может быть исключен из результатов Netmon. Исключение может возникать, если службы находятся на портах, отличных от портов по умолчанию (5357/5358), а стек DPWS не отвечает на сообщения с помощью порта по умолчанию. В таких случаях необходимо изменить фильтры перед использованием.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Процедуры диагностики WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[начало работы с разрешениями WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



