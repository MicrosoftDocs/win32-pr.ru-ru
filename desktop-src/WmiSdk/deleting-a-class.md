---
description: В отличие от удаления динамического экземпляра, удаление класса является простой процедурой.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Удаление класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad3e44292aa1ca6b534151a82f36df50802e04db788d8cfb8aaeb477c23164f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412094"
---
# <a name="deleting-a-class"></a>Удаление класса

В отличие от удаления динамического экземпляра, удаление класса является простой процедурой. Однако, как обсуждалось ранее, базовые или производные классы редко удаляются. Вместо этого экземпляр чаще всего удаляется. [API скриптов для WMI](scripting-api-for-wmi.md) использует те же методы для удаления объекта класса или экземпляра. Дополнительные сведения см. в разделе [Удаление экземпляра](deleting-an-instance.md). Сведения об удалении классов и экземпляров из репозитория WMI см. в описании команды препроцессора [**pragma делетекласс**](pragma-deleteclass.md) .

[Интерфейс API COM для WMI](com-api-for-wmi.md) имеет различные методы для удаления экземпляра и удаления объекта.

В следующей процедуре описывается удаление базового класса или производного класса.

**Удаление базового класса или производного класса**

-   Вызовите метод [**IWbemServices::D елетекласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) или [**IWbemServices::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .

    Как видно из названия, [**делетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) удаляет экземпляр асинхронно, в то время как [**делетекласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) удаляет экземпляр синхронно. Чтобы использовать **делетеклассасинк**, необходимо также реализовать объект [**ивбемобжектсинк**](iwbemobjectsink.md) .

> [!Note]  
> Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

 

 



