---
description: Для создания расширений сертификатов можно использовать следующие интерфейсы.
ms.assetid: 52750a0a-0cd9-40cc-8c23-839e4e20fd77
title: Интерфейсы расширения сертификата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c192ff7bc661c36ded8611628a1cd82dddca1697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541802"
---
# <a name="certificate-extension-interfaces"></a>Интерфейсы расширения сертификата

Для создания расширений сертификатов можно использовать следующие интерфейсы.



| Интерфейс                                                                            | Описание                                                                                                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иалтернативенаме**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename)                                         | Представляет экземпляр расширения **алтернативенамес** .                                                                                   |
| [**иалтернативенамес**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativenames)                                       | Управляет коллекцией объектов [**иалтернативенаме**](/windows/desktop/api/CertEnroll/nn-certenroll-ialternativename) .                                                                  |
| [**ицертификатеполици**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy)                                     | Указывает политику сертификатов, определяющую цель, для которой можно использовать сертификат.                                              |
| [**ицертификатеполиЦиес**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicies)                                 | Управляет коллекцией объектов [**ицертификатеполици**](/windows/desktop/api/CertEnroll/nn-certenroll-icertificatepolicy) .                                                              |
| [**иполицикуалифиер**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier)                                         | Представляет квалификатор, который может быть связан с политикой сертификата.                                                                       |
| [**иполицикуалифиерс**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifiers)                                       | Управляет коллекцией объектов [**иполицикуалифиер**](/windows/desktop/api/CertEnroll/nn-certenroll-ipolicyqualifier) .                                                                  |
| [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)                                             | Определяет расширение для запроса сертификата.                                                                                                |
| [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)             | Указывает одну или несколько альтернативных форм имен для субъекта сертификата.                                                                 |
| [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier) | Представляет расширение **аусоритикэйидентифиер** .                                                                                            |
| [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)             | Указывает, является ли субъект сертификата центром сертификации и, если да, глубиной цепочки подчиненных центров сертификации. |
| [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)       | Представляет коллекцию терминов сведений о политике.                                                                                           |
| [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)   | Представляет коллекцию идентификаторов объектов, которые указывают, как можно использовать сертификат приложением.                                   |
| [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)             | Представляет коллекцию идентификаторов объектов, определяющих предполагаемое использование открытого ключа, содержащегося в сертификате.                    |
| [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)                             | Представляет ограничения на операции, которые могут быть выполнены с помощью открытого ключа, содержащегося в сертификате.                                |
| [**IX509Extensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensions)                                           | Управляет коллекцией объектов [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) .                                                                      |
| [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)           | Представляет коллекцию, которая сообщает возможности расшифровки получателя сообщения электронной почты отправителю.                                     |
| [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)     | Представляет расширение **субжекткэйидентифиер** , используемое для распознавания сертификата подписи.                                                        |
| [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)                             | Представляет расширение **CertificateTemplate** , содержащее шаблон версии 2.                                                             |
| [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)                     | Представляет расширение **цертификатетемплатенаме** , содержащее шаблон версии 1.                                                         |
| [**исмимекапабилитиес**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapabilities)                                     | Управляет коллекцией объектов [**исмимекапабилити**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability) .                                                                  |
| [**исмимекапабилити**](/windows/desktop/api/CertEnroll/nn-certenroll-ismimecapability)                                         | Представляет расширение **смимекапабилитиес** , которое определяет возможности расшифровки получателя электронной почты.                               |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



