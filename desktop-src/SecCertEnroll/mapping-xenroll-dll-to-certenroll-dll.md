---
description: Библиотека Xenroll.dll была удалена из операционной системы и заменена CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Сопоставление Xenroll.dll CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815769"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Сопоставление Xenroll.dll CertEnroll.dll

До выхода Windows Vista Управление регистрацией сертификатов было реализовано в Xenroll.dll. Библиотека Xenroll.dll была удалена из операционной системы и заменена CertEnroll.dll.

Xenroll попытался реализовать два параллельных набора интерфейсов. [**Иценролл**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)и [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) были совместимы с автоматизацией и совместимы с языками сценариев. Соответствующие интерфейсы —[**иенролл**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)и [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)— не могут быть внесены в скрипт, но более удобны для программистов C++. По мере их развития два набора интерфейсов не сохранились синхронизированными. В частности, набор сдвоенных интерфейсов, которые в последнее время представляются **ICEnroll4** , определяет только подмножество функций, определенных **IEnroll4**.

CertEnroll.dll реализует более широкий и структурированный набор совместимых с автоматизацией COM-интерфейсов. В следующих разделах описывается, как Xenroll.dll сопоставляется CertEnroll.dll для различных типов функций.

-   [Функции запроса сертификата](certificate-request-functions.md)
-   [Функции ответа на сертификат](certificate-response-functions.md)
-   [Функции атрибутов](attribute-functions.md)
-   [Функции расширения](extension-functions.md)
-   [Функции внешних свойств](external-property-functions.md)
-   [Функции закрытых и открытых ключей](private-and-public-key-functions.md)
-   [Функции поставщика служб шифрования](cryptographic-service-provider-functions.md)
-   [Функции хранилища сертификатов](certificate-store-functions.md)
-   [Функции обмена личной информацией](personal-information-exchange-functions.md)
-   [Вспомогательные функции](helper-functions.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование API регистрации сертификатов](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
