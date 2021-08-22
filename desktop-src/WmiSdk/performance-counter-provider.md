---
description: Поставщик счетчика производительности — это высокопроизводительный поставщик, который предоставляет необработанные данные счетчиков производительности в классы счетчиков производительности WMI, производные от Win32 \_ перфравдата. \_ \_ Имя экземпляра Win32Provider — &\# 0034; ПРЕОБРАЗОВАТЬ права NT5 \_ женерикперфпровидер \_ V1&\# 0034;.
ms.assetid: 2c7206e7-f5f8-4d40-b993-56122e48069b
ms.tgt_platform: multiple
title: Поставщик счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c846d66cd183e866623004cacfbcb630ac68480fab8dd58eca2b5a4dc6d2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050532"
---
# <a name="performance-counter-provider"></a>Поставщик счетчиков производительности

\[Поставщик счетчиков производительности больше не доступен для использования. Вместо этого используйте поставщик [вмиперфинст](wmiperfinst-provider.md) .\]

Поставщик счетчика производительности — это высокопроизводительный поставщик, который предоставляет необработанные данные счетчиков производительности в [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata). Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) — "преобразовать права NT5 \_ женерикперфпровидер \_ v1".

Классы [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) находятся в пространстве имен WMI "root \\ CIMv2". Каждый класс производительности WMI соответствует объекту производительности в библиотеке производительности. Свойства этих классов представляют счетчики для объекта. Имя класса WMI для необработанного объекта счетчика имеет вид **Win32 \_ \_ \_ перфравдата* службы имя \_ *\_* объекта \_ * * *. Например, имя класса WMI, содержащего счетчики логических дисков, — [**Win32 \_ перфравдата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).

Для получения предварительно вычисленных данных производительности, отображаемых в [*системном мониторе*](gloss-s.md), можно использовать соответствующий класс [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) . Например, чтобы получить предварительно вычисленные данные диска, используйте класс [**\_ \_ \_ LogicalDisk перфформаттеддата перфдиск Win32**](./retrieving-raw-and-formatted-performance-data.md) .

Дополнительные сведения о написании клиента, который может получать доступ к необработанным данным производительности, см. [в разделе доступ к данным производительности в C++](accessing-performance-data-in-c--.md).

Как высокопроизводительный поставщик, поставщик счетчиков производительности реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , а также метод [**Ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) и следующие методы [**ивбемхиперфпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :

-   [**креатерефрешаблинум**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)
-   [**креатерефрешаблеобжект**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject)
-   [**креатерефрешер**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)
-   [**Объекты GetObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)
-   [**куеринстанцес**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)
-   [**стопрефрешинг**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Поставщики WMI](wmi-providers.md)
</dt> </dl>

 

 
