---
description: Система использует сведения о конфигурации для определения способа запуска службы.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Конфигурация службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f64b5cef835e1c7efef10c12555c81c132e707c8d1fb2814a7fcb95cf6d71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889084"
---
# <a name="service-configuration"></a>Конфигурация службы

Система использует сведения о конфигурации для определения способа запуска службы. Сведения о конфигурации также включают отображаемое имя службы и ее описание. Например, для службы DHCP можно использовать отображаемое имя "Служба протокола настройки динамического узла" и описание "предоставляет адреса Интернета для компьютера в сети".

Чтобы изменить сведения о конфигурации для объекта службы, программа настройки использует функцию [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) или [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) . Пример см. в разделе [изменение конфигурации службы](changing-a-service-configuration.md).

Чтобы получить сведения о конфигурации для объекта службы, программа настройки использует функцию [**куерисервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) или [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) . Пример см. в разделе [запросы к конфигурации службы](querying-a-service-s-configuration.md).

Функции конфигурации службы [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) и [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) поддерживают использование триггеров для управления запуском службы.

Чтобы изменить дескриптор безопасности для объекта SCManager или объекта службы, программа настройки использует функцию [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Чтобы получить копию дескриптора безопасности, программа настройки использует функцию [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка службы с помощью SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
