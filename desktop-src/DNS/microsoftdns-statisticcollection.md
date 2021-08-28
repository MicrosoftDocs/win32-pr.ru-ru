---
title: MicrosoftDNS_StatisticCollection
description: Класс Микрософтднс \_ статистикколлектион представляет коллекцию связанных статистических данных DNS-сервера.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fda276433290ab2b151b4b6a34abae7a0113ee3db75054f6c66c0536009dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109095"
---
# <a name="microsoftdns_statisticcollection"></a>Микрософтднс \_ статистикколлектион

Класс Микрософтднс \_ статистикколлектион представляет коллекцию связанных статистических данных DNS-сервера.

Следующий синтаксис упрощен из MOF-кода.

``` syntax
class MicrosoftDNS_StatisticCollection : CIM_LogicalElement
{
  string Name;
  uint32 StatId;
  MicrosoftDNS_Statistic Statistics[];
};
```

## <a name="properties"></a>Свойства

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**
</dt> <dd>

Имя статистической коллекции.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**статид**
</dt> <dd>

Числовое представление статистической коллекции.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Статистика статистики Микрософтднс \_\[\]**
</dt> <dd>

Массив значений, связанных с статистикой.

</dd> </dl>

## <a name="methods"></a>Методы

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Этот класс не имеет методов.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**\_Статистика микрософтднс**](microsoftdns-statistic.md)
</dt> </dl>

 

 




