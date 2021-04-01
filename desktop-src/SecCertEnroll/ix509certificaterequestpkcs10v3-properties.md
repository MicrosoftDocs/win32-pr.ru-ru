---
description: Интерфейс IX509CertificateRequestPkcs10V3 предоставляет следующие свойства.
ms.assetid: 96FCB9C4-7DDB-4B6B-A776-5A33E07B0BD3
title: Свойства IX509CertificateRequestPkcs10V3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4967b10e49ed015b22ffcab19726f5662937d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999514"
---
# <a name="ix509certificaterequestpkcs10v3-properties"></a>Свойства IX509CertificateRequestPkcs10V3

Интерфейс [**IX509CertificateRequestPkcs10V3**](/windows/desktop/api/Certenroll/nn-certenroll-ix509certificaterequestpkcs10v3) предоставляет следующие свойства.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                                            | Описание                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Аттестатионенкриптионцертификате, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate)<br/> | Сертификат, используемый для шифрования значений ЕКПУБ и ЕКЦЕРТ от клиента. Для этого свойства необходимо задать действительный сертификат, который связан с корнем доверенного компьютера.<br/>                                                                                                                                                                                |
| [**Аттестприватекэй, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestprivatekey)<br/>                                 | Значение true, если созданный закрытый ключ необходимо подтверждать; в противном случае — false. Если значение — true, ожидается, что свойство [**аттестатионенкриптионцертификате**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_attestationencryptioncertificate) установлено. <br/>                                                                                                        |
| [**Чалленжепассворд, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword)<br/>                               | Пароль, используемый при создании запроса с запросом. Чтобы создать запрос без запроса, не устанавливайте свойство [**чалленжепассворд**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_challengepassword) .<br/>                                                                                                                                      |
| [**EncryptionAlgorithm, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm)<br/>                           | Алгоритм шифрования, используемый для шифрования значений ЕКПУБ и ЕКЦЕРТ от клиента.<br/>                                                                                                                                                                                                                                                               |
| [**Енкриптионстренгс, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength)<br/>                             | Определяет битовую длину для [**EncryptionAlgorithm**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionalgorithm) , используемой для шифрования. Если **EncryptionAlgorithm** поддерживает только одну длину битов, не нужно указывать значение для свойства [**енкриптионстренгс**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_encryptionstrength) .<br/> |
| [**Намевалуепаирс, свойство**](/windows/desktop/api/Certenroll/nf-certenroll-ix509certificaterequestpkcs10v3-get_namevaluepairs)<br/>                                     | Коллекция пар "имя-значение" дополнительных значений свойств сертификата.<br/>                                                                                                                                                                                                                                                                         |



 

 

 




