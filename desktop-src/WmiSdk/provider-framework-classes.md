---
description: Классы C++ с WMI, которые являются частью инфраструктуры поставщика WMI, теперь считаются в конечном состоянии.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Классы инфраструктуры поставщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1562d00e6b3b1563ece933ba7dd9361dd8a5d94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712108"
---
# <a name="provider-framework-classes"></a>Классы инфраструктуры поставщиков

\[Классы C++ с WMI, которые являются частью инфраструктуры поставщика WMI, теперь считаются окончательными, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки. [API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]

Платформа поставщика реализует следующие классы.



| Класс Framework                                | Описание                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**кфрамеворккуери**](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | Содержит методы для обработки запросов.                                                                                                                                                                              |
| [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)                 | Содержит методы для установки и получения свойств и является инкапсуляцией интерфейса [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) . Разработчику не нужно напрямую обращаться к методам **ивбемклассобжект** . |
| [**ксреадбасе**](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | Базовый класс, предоставляющий механизмы безопасности внутреннего потока для платформы поставщика WMI.                                                                                                                    |
| [**квбемглуефактори**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | Часть платформы поставщика WMI. Инфраструктура поставщика реализует методы этого интерфейса для внутреннего создания новых экземпляров классов для поставщика.                                                     |
| [**квбемпровидерглуе**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | Реализует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и методы, которые управляют загрузкой и выгрузкой поставщика платформы.                                                                             |
| [**Поставщик**](/windows/desktop/api/Provider/nl-provider-provider)                   | Содержит вспомогательные функции и предоставляет реализации по умолчанию методов [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).                                                                                            |



 

Обратите внимание, что многие методы платформы используют параметры [**чстринг**](chstring.md) . **Чстринг** поддерживает многие те же методы и свойства, что и Microsoft Foundation Classes (MFC), но без затрат на MFC. Дополнительные сведения о **чстринг** см. в разделе **Справочник по классам чстринг**.

 

 
