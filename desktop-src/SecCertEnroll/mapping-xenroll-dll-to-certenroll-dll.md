---
description: Библиотека Xenroll.dll была удалена из операционной системы и заменена CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Сопоставление Xenroll.dll CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8cd2286823dbf8029896c8656807f614dc0e1994fda908cd9b13ec8ad24c7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993534"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a>Сопоставление Xenroll.dll CertEnroll.dll

до Windows Vista управление регистрацией сертификатов реализовано в Xenroll.dll. Библиотека Xenroll.dll была удалена из операционной системы и заменена CertEnroll.dll.

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
-   [персональные данные Exchange функции](personal-information-exchange-functions.md)
-   [Вспомогательные функции](helper-functions.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование API регистрации сертификатов](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
