---
description: Рекомендуется компилировать все постоянные подписки в \\ \\ пространство имен корневой подписки.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Реализация постоянных подписок на события между пространствами имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b175f89a4a686aa47818daf3479d521306f6190fb245222c4c21c17ca6470dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757954"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Реализация постоянных подписок на события между пространствами имен

Рекомендуется компилировать все постоянные подписки в \\ \\ пространство имен корневой подписки. Это предотвращает необходимость компиляции постоянного потребителя в каждое используемое пространство имен. Это означает, что существует только одно пространство имен для поиска постоянных подписок. Используйте свойство **евентнамеспаце** объекта [**\_ \_ EventFilter**](--eventfilter.md) для реализации подписки между пространствами имен.

При использовании [**коммандлинивентконсумер**](commandlineeventconsumer.md)важно защитить исполняемый файл, который вы запускаете. Если исполняемый файл не находится в безопасном месте или защищен с помощью строгого списка управления доступом (ACL), любой пользователь может заменить исполняемый файл одним из его собственных. Дополнительные сведения об ACL см. [в разделе Создание дескриптора безопасности для нового объекта в C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

В следующем примере кода MOF-файл (MOF) показана подписка на перекрестное пространство имен.

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
