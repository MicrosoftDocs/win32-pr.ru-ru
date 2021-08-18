---
description: Реализует интерфейс IX509Enrollment.
ms.assetid: bcf5c2f0-b99f-4de5-83f4-44f17dc31cd4
title: Функции ответа на сертификат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f82922ce2b0cdfad370bbfbf4d1fd3a135c19d5ba613110364f7283ec12a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902404"
---
# <a name="certificate-response-functions"></a>Функции ответа на сертификат

CertEnroll.dll реализует интерфейс [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) для отправки запроса на сертификат клиента и установки ответа от [*центра сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС).

Процесс регистрации может соответствовать следующим трем сценариям:

<dl> Нестандартная регистрация

1.  Вызовите любой метод инициализации, реализованный объектом [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) , чтобы получить запрос.
3.  Отправьте запрос из аппаратного контроллера управления (вручную или с помощью другого процесса).
4.  Получение ответа от центра сертификации.
5.  Вызовите метод [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) .

  
Автоматическая регистрация

1.  Вызовите любой метод инициализации, реализованный объектом [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) .

  
Отложенная регистрация

1.  Вызовите любой метод инициализации, реализованный объектом [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .
2.  Вызовите метод [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest) , чтобы получить запрос.
3.  Сохраните запрос, пока вы не будете готовы отправить его.
4.  Когда вы будете готовы к регистрации, вызовите метод [**Initialize**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-initialize) для повторной инициализации объекта регистрации.
5.  Вызовите метод [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) , когда ЦС возвращает сертификат.

  
</dl>

Во время процесса регистрации можно вызвать свойство [**Status**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_status) объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , чтобы получить значение перечисления [**енроллментенроллстатус**](/windows/desktop/api/CertEnroll/ne-certenroll-enrollmentenrollstatus) , определяющее, успешно ли выполнена регистрация, ожидание, пропущено, сформировано сообщение об ошибке или было отказано.

В каждом из следующих разделов указывается функция, экспортированная с помощью Xenroll.dll для установки ответа сертификата из центра сертификации. В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует:

-   [acceptFilePKCS7WStr](#acceptfilepkcs7wstr)
-   [акцептфилереспонсевстр](#acceptfileresponsewstr)
-   [acceptPKCS7Blob](#acceptpkcs7blob)
-   [акцептреспонсеблоб](#acceptresponseblob)
-   [жетцертконтекстфромфилереспонсевстр](#getcertcontextfromfileresponsewstr)
-   [getCertContextFromPKCS7](#getcertcontextfrompkcs7)
-   [жетцертконтекстфромреспонсеблоб](#getcertcontextfromresponseblob)
-   [InstallPKCS7Blob](#installpkcs7blobex)
-   [InstallPKCS7BlobEx](#installpkcs7blobex)
-   [спкфиленамевстр](#spcfilenamewstr)
-   [вритецерттоксп](#writecerttocsp)
-   [вритецерттаусердс](#writecerttouserds)
-   [Связанные темы](#related-topics)

## <a name="acceptfilepkcs7wstr"></a>acceptFilePKCS7WStr

Функция [**acceptFilePKCS7WStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr) в Xenroll.dll устанавливает ответ [*PKCS \# 7*](/windows/desktop/SecGloss/p-gly) из файла.

Библиотека CertEnroll.dll напрямую не реализует функции для установки \# ответа сертификата PKCS 7 из файла. Однако можно создать пользовательскую функцию для чтения файловых данных в массив байтов и вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) для установки ответа.

Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, тем самым позволяя установить сертификат без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="acceptfileresponsewstr"></a>акцептфилереспонсевстр

Функция [**акцептфилереспонсевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptfileresponsewstr) в Xenroll.dll устанавливает \# ответ на сертификат PKCS 7 или CMC из файла.

Библиотека CertEnroll.dll не реализует напрямую функции для установки ответа на сертификат из файла. Однако можно создать пользовательскую функцию для чтения файловых данных в массив байтов и вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) для установки \# ответа PKCS 7 или CMC.

Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, тем самым позволяя установить сертификат без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="acceptpkcs7blob"></a>acceptPKCS7Blob

Функция [**acceptPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob) в Xenroll.dll устанавливает \# ответ PKCS 7, содержащийся в массиве байтов.

Чтобы установить сообщение PKCS 7, можно вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) \# . Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, тем самым позволяя установить \# ответ PKCS 7 без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="acceptresponseblob"></a>акцептреспонсеблоб

Функция [**акцептреспонсеблоб**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-acceptresponseblob) в Xenroll.dll устанавливает \# ответ на сертификат PKCS 7 или CMC, содержащийся в массиве байтов.

Вы можете вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) , чтобы установить \# ответ PKCS 7 или CMC. Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, что позволит установить ответ без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="getcertcontextfromfileresponsewstr"></a>жетцертконтекстфромфилереспонсевстр

Функция [**жетцертконтекстфромфилереспонсевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromfileresponsewstr) в Xenroll.dll извлекает сертификат клиента из файла.

Библиотека CertEnroll.dll напрямую не реализует функции для получения сертификата из ответа центра сертификации, сохраненного в файле. Однако можно создать пользовательскую функцию для чтения файловых данных в массив байтов и вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) для установки \# ответа PKCS 7 или CMC и вызвать свойство [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) для получения сертификата.

Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, тем самым позволяя установить сертификат без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="getcertcontextfrompkcs7"></a>getCertContextFromPKCS7

Функция [**getCertContextFromPKCS7**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-getcertcontextfrompkcs7) в Xenroll.dll извлекает сертификат клиента из \# ответа PKCS 7.

Чтобы получить сертификат после вызова метода [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) , можно вызвать свойство [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .

## <a name="getcertcontextfromresponseblob"></a>жетцертконтекстфромреспонсеблоб

Функция [**жетцертконтекстфромреспонсеблоб**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-getcertcontextfromresponseblob) в Xenroll.dll извлекает сертификат клиента из \# ответа PKCS 7 или CMC.

Чтобы получить сертификат после вызова метода [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) , можно вызвать свойство [**Certificate**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-get_certificate) объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .

## <a name="installpkcs7blob"></a>InstallPKCS7Blob

Функция [**InstallPKCS7Blob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-installpkcs7blob) в Xenroll.dll устанавливает \# ответ PKCS 7.

Вы можете вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) , чтобы установить \# ответ PKCS 7 или CMC. Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, что позволит установить ответ без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="installpkcs7blobex"></a>InstallPKCS7BlobEx

Функция [**InstallPKCS7BlobEx**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-installpkcs7blobex) в Xenroll.dll устанавливает \# ответ PKCS 7 и возвращает число установленных сертификатов.

Вы можете вызвать [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) , чтобы установить \# ответ PKCS 7 или CMC. Если указать значение **алловнуутстандингрекуест** перечисления [**инсталлреспонсерестриктионфлагс**](/windows/desktop/api/CertEnroll/ne-certenroll-installresponserestrictionflags) для первого параметра [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse), то не требуется наличие фиктивного сертификата, что позволит установить ответ без предварительного вызова функции [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) или [**креатерекуест**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createrequest). Однако если вы устанавливаете сертификат с помощью веб-скрипта, в хранилище запросов должен присутствовать фиктивный сертификат. Поэтому необходимо указать **алловноне** для первого параметра.

## <a name="spcfilenamewstr"></a>спкфиленамевстр

Функция [**спкфиленамевстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_spcfilenamewstr) в Xenroll.dll указывает или получает имя файла, в котором следует сохранить ответ сертификата. Библиотека CertEnroll.dll не реализует функциональность, позволяющую копировать сертификат в конкретный файл. Процесс регистрации автоматически устанавливает цепочку сертификатов в файлы в соответствующих хранилищах.

## <a name="writecerttocsp"></a>вритецерттоксп

Функция [**вритецерттоксп**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttocsp) в Xenroll.dll указывает или получает логическое значение, указывающее, должен ли сертификат быть записан в [*поставщик служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP). Как правило, при вызове этой функции поставщик является [*смарт-картой*](/windows/desktop/SecGloss/s-gly).

В CertEnroll.dll, когда клиент вызывает метод [**регистрации**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) для отправки запроса на сертификат смарт-карты и выдается сертификат, [**Регистрация**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) автоматически устанавливает сертификат на смарт-карту при условии, что карта установлена в модуле чтения. Метод [**инсталлреспонсе**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-installresponse) также автоматически записывает сертификат на смарт-карту.

## <a name="writecerttouserds"></a>вритецерттаусердс

Функция [**вритецерттаусердс**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_writecerttouserds) в Xenroll.dll указывает или получает логическое значение, указывающее, следует ли сохранять сертификат в хранилище Active Directory. Библиотека CertEnroll.dll не реализует функциональность, позволяющую указать хранилище для копирования сертификата.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сопоставление Xenroll.dll CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
