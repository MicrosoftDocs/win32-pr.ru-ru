---
description: Регистрация конечного пользователя в центре сертификации (ЦС) с помощью шаблона, имени субъекта и длины (в битах) ключа.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: енроллсимплеусерцерт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4763e3ae68404e47207dccdb75c759fc30394e849bee07a71f2c54c649347a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119669914"
---
# <a name="enrollsimpleusercert"></a>енроллсимплеусерцерт

Пример Енроллсимплеусерцерт регистрирует конечного пользователя в центре сертификации (ЦС) с помощью шаблона, имени субъекта и длины ключа в битах.

## <a name="location"></a>Расположение

при установке пакета средств разработки Microsoft Windows Software Development Kit (SDK) версия C++ образца по умолчанию устанавливается в папку *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Security ssl \\ Certificate \\ \\ енроллсимплеусерцерт. версия C# установлена в папке *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples, посвященной \\ регистрации сертификата X509 в \\ \\ каталоге CSharp енроллсимплеусерцерт.

## <a name="discussion"></a>Разговор

Пример Енроллсимплеусерцерт:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать имя шаблона, имя субъекта и длину ключа.
2.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и инициализирует его с помощью шаблона.
3.  Извлекает объект запроса внутреннего сертификата из объекта регистрации и запрашивает его для объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . Самый внутренний запрос всегда является \# запросом PKCS 10.
4.  Извлекает объект [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) из \# запроса PKCS 10 и задает длину ключа, указанную в командной строке.
5.  Создает объект [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , использует его для кодирования имени субъекта X. 500 и добавляет имя в \# запрос PKCS 10.
6.  Пытается зарегистрировать конечного пользователя в центре сертификации и отслеживать ход процесса регистрации. Функция Чеккенроллстатус определена в Енроллкоммон. cpp.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 



