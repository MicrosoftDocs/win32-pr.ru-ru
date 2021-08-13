---
description: Вычисляемые блоки (&\# 0034; обработанные&\# 0034;) данные счетчика производительности. Предоставляет динамические данные классам WMI, производным от Win32 \_ перфформаттеддата. Также известен как поставщик счетчика обработанные.
ms.assetid: 59823f7c-3046-4608-99df-1f43e2934e7e
ms.tgt_platform: multiple
title: Поставщик форматированных данных о производительности
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab8e931c3d03c619af5b1e37cadd8dacdccd21534513ed3a1aa1d7b9076acfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556617"
---
# <a name="formatted-performance-data-provider"></a>Поставщик форматированных данных о производительности

\[Отформатированный поставщик данных о производительности, также известный как "поставщик счетчиков обработанные", больше недоступен для использования. Вместо этого используйте поставщик [вмиперфинст](wmiperfinst-provider.md) .\]

Высокопроизводительный поставщик данных о производительности предоставляет вычисленные ("обработанные") данные счетчика производительности, например процент времени, затрачиваемого диском на запись данных. Этот поставщик предоставляет динамические данные классам WMI, производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Различие между этим поставщиком и [поставщиком счетчика производительности](performance-counter-provider.md) заключается в том, что поставщик счетчика производительности предоставляет необработанные данные, а поставщик счетчиков обработанные предоставляет данные производительности, которые отображаются в точности так же, как в [*системном мониторе*](gloss-s.md). Имя экземпляра [**\_ \_ Win32Provider**](--win32provider.md) — "хиперфкукер \_ v1".

Имя класса в формате WMI для объекта счетчика имеет вид "Win32 \_ перфформаттеддата \_ *Service \_* Name \_ *Object \_* Name". Например, имя класса WMI, содержащего счетчики логических дисков, — **Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**. Эти классы находятся в \\ пространстве имен root CIMv2.

Поскольку классы данных о производительности добавляются и изменяются динамически в определенной системе, невозможно формально документировать свойства всех известных объектов производительности. Чтобы определить, какие классы доступны для вас, а также определить, какие члены имеют эти классы, см. статью [получение документации по необработанным и форматированным объектам данных о производительности](retrieving-raw-and-formatted-performance-data.md).

Классы [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) используют квалификатор **кукингтипе** в [типах счетчиков производительности WMI](wmi-performance-counter-types.md) для указания формулы для вычисления данных о производительности. Этот квалификатор совпадает с квалификатором **CounterType** в классах [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .

Как высокопроизводительный поставщик, поставщик счетчиков обработанные реализует стандартный интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , а также метод [**Ивбемрефрешер:: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) и следующие методы [**ивбемхиперфпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) :

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

 

 
