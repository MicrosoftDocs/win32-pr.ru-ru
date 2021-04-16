---
description: Поставщик свойств извлекает и изменяет отдельные значения свойств для экземпляров заданного класса, хранящегося в репозитории WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Создание поставщика свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712093"
---
# <a name="writing-a-property-provider"></a>Создание поставщика свойств

Поставщик свойств извлекает и изменяет отдельные значения свойств для экземпляров заданного класса, хранящегося в репозитории WMI.

В следующей процедуре описывается создание поставщика свойств.

**Создание поставщика свойств**

1.  Разработка и регистрация поставщика с помощью WMI.

    Поставщики экземпляров регистрируются в WMI путем создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ пропертипровидеррегистратион**](--propertyproviderregistration.md) . Дополнительные сведения см. [в разделе Регистрация поставщика свойств](registering-a-property-provider.md).

2.  Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.

    Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика. Это задача, общая для всех поставщиков. Дополнительные сведения см. [в разделе Инициализация поставщика](initializing-a-provider.md).

    > [!Note]  
    > Поставщики свойств настоятельно рекомендуется использовать модель многопоточности "both".

     

3.  Реализуйте интерфейс [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) для поставщика.

    Интерфейс [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) является основным интерфейсом для поставщика свойств. Двумя основными методами являются [**Свойства**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) [**putproperty изменил**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty)и. Дополнительные сведения см. [в разделе Реализация основного интерфейса для поставщика свойств](implementing-the-primary-interface-for-a-property-provider.md).

4.  Добавьте дополнительный код, необходимый для поставщика.

    При проектировании поставщика вам, скорее всего, придется вызывать интерфейсы WMI. Дополнительные сведения см. в разделе [вызов метода](calling-a-method.md) и [обслуживание уровней безопасности в поставщике](impersonating-a-client.md).

    При получении сведений для клиента может потребоваться доступ к уровням безопасности для этого клиента. Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).

5.  Замените имеющийся поставщик новым кодом.

    Вам не нужно выполнять этот шаг, если у вас нет уже существующего поставщика для копирования. Дополнительные сведения см. [в разделе Обновление поставщика](updating-a-provider.md).

 

 



