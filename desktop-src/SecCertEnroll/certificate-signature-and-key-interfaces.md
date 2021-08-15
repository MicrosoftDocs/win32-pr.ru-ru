---
description: Для управления подписями сертификатов, а также открытыми и закрытыми ключами можно использовать следующие интерфейсы.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Сигнатуры сертификата и интерфейсы ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bdfd4c76b0e73f2954780d797e092e6d8b7570ebaee082ef93319f74abc24e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902310"
---
# <a name="certificate-signature-and-key-interfaces"></a>Сигнатуры сертификата и интерфейсы ключей

Для управления подписями сертификатов, а также открытыми и закрытыми ключами можно использовать следующие интерфейсы.



| Интерфейс                                                      | Описание                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | Представляет сертификат подписи, позволяющий подписывать запрос на сертификат.                  |
| [**исигнерцертификатес**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | Управляет коллекцией объектов [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .                 |
| [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | Представляет асимметричный закрытый ключ, который можно использовать для шифрования, подписи и соглашения о ключах. |
| [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | Представляет открытый ключ в паре открытого и закрытого ключей.                                             |
| [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | Представляет сведения, используемые для подписания запроса на сертификат.                                        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



