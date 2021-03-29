---
description: Для создания атрибутов сертификата можно использовать следующие интерфейсы.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Интерфейсы атрибутов сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647175"
---
# <a name="certificate-attribute-interfaces"></a>Интерфейсы атрибутов сертификата

Для создания атрибутов сертификата можно использовать следующие интерфейсы.



| Интерфейс                                                                    | Описание                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | Представляет криптографический атрибут в запросе на сертификат.                                                                              |
| [**икриптаттрибутес**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | Управляет коллекцией объектов [**икриптаттрибуте**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | Представляет атрибут в \# запросе сертификата PKCS 7, PKCS \# 10 или CMC.                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | Представляет атрибут, который может использоваться для распознавания клиента, создавшего запрос на сертификат.                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | Представляет расширения сертификата в запросе на сертификат.                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | Представляет атрибут, содержащий зашифрованный закрытый ключ, заархивированный центром сертификации.                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | Представляет атрибут, содержащий хэш SHA-1 зашифрованного закрытого ключа, который должен быть архивирован центром сертификации.                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | Представляет атрибут, определяющий поставщик служб шифрования, используемый сущностью, запрашивающей сертификат.                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | Представляет атрибут, содержащий сведения о версии клиентской операционной системы, на которой был создан запрос сертификата. |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | Представляет атрибут, который содержит обновляемый сертификат.                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | Управляет коллекцией объектов [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | Представляет пару "имя-значение".                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | Управляет коллекцией объектов [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .                                                           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



