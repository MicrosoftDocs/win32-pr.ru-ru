---
description: Функции, экспортированные Xenroll.dll, которые можно использовать для управления поставщиком служб шифрования.
ms.assetid: 4f6f353d-6b06-45b4-8808-56998d3727a4
title: Функции поставщика служб шифрования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947d9c4f2529071b28052ae5ca34f811d4657c3fd4cede23285999cbaa13a72c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883084"
---
# <a name="cryptographic-service-provider-functions"></a>Функции поставщика служб шифрования

В каждом из следующих разделов указывается функция, экспортируемая с помощью Xenroll.dll, которую можно использовать для управления поставщиком служб шифрования. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:

-   [енумалгс](#enumalgs)
-   [енумконтаинерсвстр](#enumcontainerswstr)
-   [енумпровидерсвстр](#enumproviderswstr)
-   [жеталгнамевстр](#getalgnamewstr)
-   [жетпровидертипевстр](#getprovidertypewstr)
-   [хашалгид](#hashalgid)
-   [хашалгорисмвстр](#hashalgorithmwstr)
-   [провидерфлагс](#providerflags)
-   [провидернамевстр](#providernamewstr)
-   [ProviderType](#getprovidertypewstr)
-   [Связанные темы](#related-topics)

## <a name="enumalgs"></a>енумалгс

Функция [**енумалгс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-enumalgs) в Xenroll.dll извлекает коллекцию алгоритмов шифрования.

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить сведения о алгоритмах, поддерживаемых [*поставщиком служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP).

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**кспинформатионс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , полученного на шаге 4.
6.  Вызовите свойство [**кспалгорисмс**](/windows/desktop/api/CertEnroll/nf-certenroll-icspinformation-get_cspalgorithms) для определенного объекта [**Икспинформатион**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) в коллекции [**икспинформатионс**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) , полученной на шаге 5.

## <a name="enumcontainerswstr"></a>енумконтаинерсвстр

Функция [**енумконтаинерсвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumcontainerswstr) в Xenroll.dll извлекает контейнер ключей из коллекции по индексу.

Библиотека CertEnroll.dll не реализует эту функцию напрямую.

## <a name="enumproviderswstr"></a>енумпровидерсвстр

Функция [**енумпровидерсвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-enumproviderswstr) в Xenroll.dll извлекает CSP из коллекции по индексу.

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить коллекцию криптографических контейнеров:

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**кспинформатионс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_cspinformations) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , полученного на шаге 4.

## <a name="getalgnamewstr"></a>жеталгнамевстр

Функция [**жеталгнамевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getalgnamewstr) в Xenroll.dll извлекает имя [*алгоритма шифрования*](/windows/desktop/SecGloss/c-gly).

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить имя алгоритма:

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**Algorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_algorithm) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , чтобы получить идентификатор объекта алгоритма.
6.  Вызовите свойство [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) в интерфейсе [**иобжектид**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , чтобы получить отображаемое имя алгоритма.

## <a name="getprovidertypewstr"></a>жетпровидертипевстр

Функция [**жетпровидертипевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getprovidertypewstr) в Xenroll.dll Извлекает тип поставщика служб шифрования.

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить тип поставщика:

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , полученное на шаге 4.

## <a name="hashalgid"></a>хашалгид

Функция [**хашалгид**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_hashalgid) в Xenroll.dll извлекает целочисленное значение, содержащее идентификатор алгоритма, используемого для подписания запроса.

При использовании CertEnroll.dll можно выполнить следующие действия для получения алгоритма хэширования:

-   Получите интерфейс [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) путем вызова свойства [**СИГНАТУРЕИНФОРМАТИОН**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) в \# запросе PKCS 10 или CMC или свойства [**сигнерцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) в запросе [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) .
-   Вызовите свойство [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) объекта сведений о сигнатуре, чтобы получить идентификатор объекта хэш-алгоритма.

## <a name="hashalgorithmwstr"></a>хашалгорисмвстр

Функция [**хашалгорисмвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_hashalgorithmwstr) в Xenroll.dll указывает или получает строковое значение, идентифицирующее алгоритм хэширования, используемый для подписания запроса.

При использовании CertEnroll.dll можно выполнить следующие действия для получения алгоритма хэширования:

-   Получите интерфейс [**IX509SignatureInformation**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) путем вызова свойства [**СИГНАТУРЕИНФОРМАТИОН**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-get_signatureinformation) в \# запросе PKCS 10 или CMC или свойства [**сигнерцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-get_signercertificate) в \# запросе PKCS 7.
-   Вызовите свойство [**HashAlgorithm**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509signatureinformation-get_hashalgorithm) объекта сведений о сигнатуре, чтобы получить идентификатор объекта хэш-алгоритма.
-   Вызовите свойство [**FriendlyName**](/windows/desktop/api/CertEnroll/nf-certenroll-iobjectid-get_friendlyname) в интерфейсе [**иобжектид**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) , возвращенном на шаге 2, чтобы получить отображаемое имя алгоритма.

## <a name="providerflags"></a>провидерфлагс

Функция [**провидерфлагс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providerflags) в Xenroll.dll указывает или получает флаги, используемые при получении маркера CSP.

Библиотека CertEnroll.dll не сопоставляет эту функцию идеально, но вы можете получить подробные сведения о свойствах из объекта регистрации и [*закрытого ключа*](/windows/desktop/SecGloss/p-gly). Для получения дополнительных сведений изучите свойства, предоставляемые интерфейсами [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) .

## <a name="providernamewstr"></a>провидернамевстр

Функция [**провидернамевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providernamewstr) в Xenroll.dll указывает или получает имя CSP.

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить имя поставщика:

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**providerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providername) для объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , полученного на шаге 4.

## <a name="providertype"></a>ProviderType

Функция [**ProviderType**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_providertype) в Xenroll.dll указывает или получает целочисленное значение, идентифицирующее тип CSP.

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить тип поставщика:

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**ProviderType**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_providertype) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , полученное на шаге 4.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**икспалгорисм**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm)
</dt> <dt>

[**икспалгорисмс**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithms)
</dt> <dt>

[**икспинформатион**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation)
</dt> <dt>

[**икспинформатионс**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> <dt>

[**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)
</dt> </dl>

 

 
