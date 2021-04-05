---
description: Для управления подписями сертификатов, а также открытыми и закрытыми ключами можно использовать следующие интерфейсы.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Сигнатуры сертификата и интерфейсы ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911288"
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Интерфейсы Цертенролл](certenroll-interfaces.md)
</dt> </dl>

 

 



