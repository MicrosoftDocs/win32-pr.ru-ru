---
description: Свойства используются для связывания значения с сертификатом.
ms.assetid: a6433416-fe77-4bb0-bd8e-9410a49ab861
title: Функции внешних свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c8148022bf604aa90780787c068b330c469ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266117"
---
# <a name="external-property-functions"></a>Функции внешних свойств

Свойства используются для связывания значения с сертификатом. Свойства никогда не отправляются или не обрабатываются [*центром сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) и не хранятся в сертификате. Как правило, они связаны с сертификатом после получения сертификата из центра сертификации и перед его сохранением в хранилище. Свойства сохраняются в хранилище вместе с сертификатом. CertEnroll.dll реализует интерфейс [**ицертпроперти**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) и следующие интерфейсы, производные от **ицертпроперти**:

-   [**ицертпропертярчивед**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)
-   [**ицертпропертярчиведкэйхаш**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)
-   [**ицертпропертяутоенролл**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)
-   [**ицертпропертибаккедуп**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)
-   [**ицертпропертидескриптион**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)
-   [**ицертпропертенроллмент**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)
-   [**ицертпропертифриендлинаме**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)
-   [**ицертпропертикэйпровинфо**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)
-   [**ицертпропертиреневал**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)
-   [**ицертпропертирекуесторигинатор**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)
-   [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash)

В каждом из следующих разделов определяется функция, экспортируемая с помощью Xenroll.dll для управления свойствами внешнего сертификата. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:

-   [аддблобпропертитоцертификатевстр](#addblobpropertytocertificatewstr)
-   [жетприватекэйарчивецертификате](#getprivatekeyarchivecertificate)
-   [ресетблобпропертиес](#resetblobproperties)
-   [сетприватекэйарчивецертификате](#setprivatekeyarchivecertificate)
-   [сетсигнерцертификате](#setsignercertificate)
-   [сумбпринтвстр](#thumbprintwstr)
-   [См. также](#related-topics)

## <a name="addblobpropertytocertificatewstr"></a>аддблобпропертитоцертификатевстр

Функция [**аддблобпропертитоцертификатевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-addblobpropertytocertificatewstr) в Xenroll.dll добавляет свойство к сертификату.

В CertEnroll.dll все объекты, производные от [**ицертпроперти**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) , реализуют метод [**сетвалуеонцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-setvalueoncertificate) , который можно использовать для связывания свойства с сертификатом. Кроме того, объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) напрямую реализует свойства [**CertificateFriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname) и [**цертификатедескриптион**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificatedescription) .

## <a name="getprivatekeyarchivecertificate"></a>жетприватекэйарчивецертификате

Функция [**жетприватекэйарчивецертификате**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprivatekeyarchivecertificate) в Xenroll.dll извлекает сертификат Exchange, используемый для архивации [*закрытого ключа*](/windows/desktop/SecGloss/p-gly).

Вы можете использовать объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) в CertEnroll.dll, чтобы создать запрос к центру сертификации для архивации закрытого ключа. Необходимо получить сертификат Exchange из центра сертификации и использовать [*открытый ключ*](/windows/desktop/SecGloss/p-gly) , содержащийся в этом сертификате, для шифрования закрытого ключа, отправляемого для архивации. Чтобы указать или получить сертификат обмена ЦС, вызовите свойство [**кэйарчивалцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) этого объекта.

## <a name="resetblobproperties"></a>ресетблобпропертиес

Функция [**ресетблобпропертиес**](/windows/desktop/api/xenroll/nf-xenroll-icenroll4-resetblobproperties) в Xenroll.dll удаляет коллекцию свойств из сертификата.

В CertEnroll.dll все объекты свойств, производные от [**ицертпроперти**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) , реализуют свойство [**ремовефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-icertproperty-removefromcertificate) , которое можно использовать для отсвязи свойства от сертификата.

## <a name="setprivatekeyarchivecertificate"></a>сетприватекэйарчивецертификате

Функция [**сетприватекэйарчивецертификате**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setprivatekeyarchivecertificate) в Xenroll.dll указывает сертификат Exchange, используемый для архивации закрытого ключа.

Вы можете использовать объект [**IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc) в CertEnroll.dll, чтобы создать запрос к центру сертификации для архивации закрытого ключа. Необходимо получить сертификат Exchange из центра сертификации и использовать открытый ключ, содержащийся в этом сертификате, для шифрования закрытого ключа, отправляемого для архивации. Чтобы указать или получить сертификат обмена ЦС, вызовите свойство [**кэйарчивалцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_keyarchivalcertificate) этого объекта.

## <a name="setsignercertificate"></a>сетсигнерцертификате

Функция [**сетсигнерцертификате**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-setsignercertificate) в Xenroll.dll указывает сертификат подписавший.

Объект [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) в CertEnroll.dll может использоваться для подписания запроса [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly), CMC или самозаверяющего [*сертификата*](/windows/desktop/SecGloss/c-gly). Вы можете инициализировать объект, используя существующий сертификат подписи, и связать его с запросом, вызвав одно из следующих свойств:

-   [**Сигнерцертификатес**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcmc-get_signercertificates) в [ **IX509CertificateRequestCmc**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcmc)
-   [**Сигнерцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) в [ **IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7)
-   [**Сигнерцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestcertificate-get_signercertificate) в [ **IX509CertificateRequestCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestcertificate)

Кроме того, при инициализации запроса CMC из внутреннего запроса и шаблона или инициализации \# запроса PKCS 7 из существующего запроса может быть установлен сертификат подписи.

## <a name="thumbprintwstr"></a>сумбпринтвстр

Функция [**сумбпринтвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-get_thumbprintwstr) в Xenroll.dll указывает или получает значение хэша сертификата.

В CertEnroll.dll можно использовать объект [**ICertPropertySHA1Hash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertysha1hash) для получения [*хэш-*](/windows/desktop/SecGloss/h-gly) значения ([*отпечатка*](/windows/desktop/SecGloss/t-gly)), созданного путем вызова метода [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
