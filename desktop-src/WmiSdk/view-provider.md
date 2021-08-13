---
description: Поставщик представления является экземпляром и поставщиком метода, который создает новые классы на основе экземпляров других классов.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Просмотр поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec84f3a22a777da2212dcfe918f4294495ade54191cd4d37e17f2ac32c2f5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553269"
---
# <a name="view-provider"></a>Просмотр поставщика

Поставщик представления является экземпляром и поставщиком метода, который создает новые классы на основе экземпляров других классов. Поставщик представлений можно использовать для получения свойств из различных исходных классов, разных пространств имен или различных компьютеров и объединения свойств в виде одного класса.

Как экземпляр и поставщик метода, поставщик представления поддерживает стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и следующие методы [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) :

-   [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Дополнительные сведения об квалификаторах, используемых для определения классов поставщиков представления, см. в разделе [квалификаторы, относящиеся к поставщику представления](qualifiers-specific-to-the-view-provider.md).

Дополнительные сведения о представлениях см. в разделе [связывание классов вместе](linking-classes-together.md).

На 64-разрядных платформах доступны две версии поставщика представления. Дополнительные сведения см. в разделе [Получение и предоставление данных на 64-разрядном компьютере](getting-and-providing-data-on-a-64-bit-computer.md).

Поставщик представления реализуется в ViewProv.dll.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поставщики WMI](wmi-providers.md)
</dt> </dl>

 

 



