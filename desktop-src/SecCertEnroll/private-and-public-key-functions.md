---
description: Реализует интерфейсы IX509PrivateKey и IX509PublicKey.
ms.assetid: 1358053e-ed4e-4482-b160-5b9b1024c771
title: Функции закрытых и открытых ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6f210393ffaeb676e0190d391692225f25e0cfb4bc3acbcd2c3c188bf40a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774427"
---
# <a name="private-and-public-key-functions"></a>Функции закрытых и открытых ключей

CertEnroll.dll реализует интерфейсы [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) и [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) . Например, можно использовать интерфейс [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) для выполнения следующих действий с [*закрытым ключом*](/windows/desktop/SecGloss/p-gly):

-   Создание, открытие, закрытие, импорт, экспорт и удаление ключа.
-   Укажите или получите [*алгоритм открытого ключа*](/windows/desktop/SecGloss/p-gly).
-   Укажите или получите сведения о доступном [*поставщике служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP), поддерживающем алгоритм открытого ключа.
-   Укажите или получите [*сертификат*](/windows/desktop/SecGloss/c-gly) , связанный с [*закрытым ключом*](/windows/desktop/SecGloss/p-gly).
-   Укажите или получите имя [*контейнера ключей*](/windows/desktop/SecGloss/k-gly).
-   Укажите или получите описание и отображаемое имя ключа.
-   Укажите или получите ограничения экспорта для закрытого ключа.
-   Укажите или получите логическое значение, указывающее, существует ли ключ.
-   Укажите или извлеките значение, указывающее, как ключ защищается перед использованием.
-   Укажите или извлеките значение, указывающее, можно ли использовать ключ для подписывания, шифрования или и того, и другого.
-   Укажите или извлеките значение, определяющее конкретную цель, для которой можно использовать ключ.
-   Укажите или получите длину ключа.
-   Укажите или извлеките значение, указывающее, используется ли ключ или сохранен в контексте компьютера или пользователя.
-   Получение логического значения, указывающего, был ли открыт ключ.
-   Укажите личный идентификационный номер для доступа к закрытому ключу на [*смарт-карте*](/windows/desktop/SecGloss/s-gly).
-   Укажите или получите имя CSP, связанного с ключом.
-   Укажите или получите [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) для ключа.

В каждом из следующих разделов определяется функция, экспортируемая с помощью Xenroll.dll, которую можно использовать для управления [*криптографическим ключом*](/windows/desktop/SecGloss/c-gly). В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:

-   [контаинернамевстр](#containernamewstr)
-   [женкэйфлагс](#genkeyflags)
-   [жеткэйлен](#getkeylenex)
-   [жеткэйленекс](#getkeylenex)
-   [жетсуппортедкэйспек](#getsupportedkeyspec)
-   [KeySpec](#getsupportedkeyspec)
-   [лимитексчанжекэйтоенЦифермент](#limitexchangekeytoencipherment)
-   [пвкфиленамевстр](#pvkfilenamewstr)
-   [реусехардварекэйифунаблетоженнев](#reusehardwarekeyifunabletogennew)
-   [усиксистингкэйсет](#useexistingkeyset)
-   [Связанные темы](#related-topics)

## <a name="containernamewstr"></a>контаинернамевстр

Функция [**контаинернамевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_containernamewstr) в Xenroll.dll указывает или получает имя [*контейнера ключей*](/windows/desktop/SecGloss/k-gly).

При использовании CertEnroll.dll можно выполнить следующие действия, чтобы получить имя контейнера ключей:

1.  Вызовите свойство [**request**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_request) для существующего объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**жетиннеррекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequest-getinnerrequest) для запроса, возвращенного на шаге 1, чтобы получить самый внутренний запрос.
3.  Вызовите **QueryInterface** для объекта [**IX509CertificateRequest**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequest) , возвращенного из шага 2, для приведения к объекту [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .
4.  Вызовите свойство [**PrivateKey**](/windows/desktop/SecCrypto/privatekey) в запросе PKCS \# 10.
5.  Вызовите свойство [**ContainerName**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_containername) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , полученного на шаге 4.

## <a name="genkeyflags"></a>женкэйфлагс

Функция [**женкэйфлагс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_genkeyflags) , определенная в Xenroll.dll указывает или получает флаги, используемые для создания пары закрытого или [*открытого и закрытого ключей*](/windows/desktop/SecGloss/p-gly).

При использовании CertEnroll.dll можно указать ряд различных свойств, определяющих способ создания закрытого ключа. Дополнительные сведения см. в разделе [**CREATE**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-create).

## <a name="getkeylen"></a>жеткэйлен

Функция [**жеткэйлен**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getkeylen) , определенная в Xenroll.dll, получает максимальный или минимальный размер ключа шифрования.

При использовании CertEnroll.dll можно вызвать свойство [**length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) или [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) , чтобы получить размер ключа в битах.

## <a name="getkeylenex"></a>жеткэйленекс

Функция [**жеткэйленекс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getkeylenex) , определенная в Xenroll.dll, получает максимальный или минимальный размер ключа или длину приращения ключа шифрования.

При использовании CertEnroll.dll можно вызвать свойство [**length**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_length) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) или [**IX509PublicKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey) , чтобы получить размер ключа в битах. Если алгоритм поддерживает добавочную длину ключей, можно вызвать свойство [**инкрементленгс**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_incrementlength) объекта [**икспалгорисм**](/windows/desktop/api/CertEnroll/nn-certenroll-icspalgorithm) , чтобы получить значение приращения. Можно также вызвать свойства [**minLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_minlength) и [**MaxLength**](/windows/desktop/api/CertEnroll/nf-certenroll-icspalgorithm-get_maxlength) , чтобы получить минимальный и максимальный размеры ключей.

## <a name="getsupportedkeyspec"></a>жетсуппортедкэйспек

Функция [**жетсуппортедкэйспек**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-getsupportedkeyspec) , определенная в Xenroll.dll, извлекает значение, указывающее, поддерживает ли CSP ключи обмена, ключи подписывания или и то, и другое.

При использовании CertEnroll.dll можно вызвать свойство [**keySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) для объектов [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) или [**икспинформатион**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformation) , чтобы получить операции, поддерживаемые ключом.

## <a name="keyspec"></a>KeySpec

Функция [**keySpec**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_keyspec) , определенная в Xenroll.dll указывает или получает тип ключа.

При использовании CertEnroll.dll можно вызвать свойство [**keySpec**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-get_keyspec) объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) для получения операций, поддерживаемых ключом.

## <a name="limitexchangekeytoencipherment"></a>лимитексчанжекэйтоенЦифермент

Функция [**лимитексчанжекэйтоенЦифермент**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_limitexchangekeytoencipherment) , определенная в Xenroll.dll указывает или получает логическое значение, указывающее, можно ли использовать ключ шифрования только для защиты данных или шифрования ключей.

CertEnroll.dll не содержит прямого эквивалента для этой функции. Однако можно добиться почти эквивалентного результата, указав объект [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage) и добавив его в запрос сертификата.

## <a name="pvkfilenamewstr"></a>пвкфиленамевстр

Функция [**пвкфиленамевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_pvkfilenamewstr) , определенная в Xenroll.dll, указывает или получает имя файла, содержащего экспортированные ключи.

При использовании CertEnroll.dll можно вызвать метод [**Export**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-export) для объекта [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) , чтобы экспортировать ключ в **BSTR**. Можно вызвать метод [**експортпубликкэй**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509privatekey-exportpublickey) для экспорта [*открытого ключа*](/windows/desktop/SecGloss/p-gly) из пары асимметричных ключей.

## <a name="reusehardwarekeyifunabletogennew"></a>реусехардварекэйифунаблетоженнев

Функция [**реусехардварекэйифунаблетоженнев**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-get_reusehardwarekeyifunabletogennew) , определенная в Xenroll.dll указывает или получает логическое значение, указывающее, используется ли существующий ключ при обнаружении ошибки при создании нового ключа.

При использовании CertEnroll.dll можно вызвать метод [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) для объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и указать значение типа перечисления [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) для повторного использования существующего закрытого ключа.

## <a name="useexistingkeyset"></a>усиксистингкэйсет

Функция [**усиксистингкэйсет**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_useexistingkeyset) , определенная в Xenroll.dll, указывает или получает логическое значение, указывающее, следует ли использовать существующие ключи.

При использовании CertEnroll.dll можно вызвать метод [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs10-initializefromcertificate) для объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) и указать значение типа перечисления [**X509RequestInheritOptions**](/windows/desktop/api/CertEnroll/ne-certenroll-x509requestinheritoptions) для повторного использования существующих закрытых и открытых ключей.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

 
