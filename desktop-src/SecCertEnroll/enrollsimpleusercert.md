---
description: Регистрация конечного пользователя в центре сертификации (ЦС) с помощью шаблона, имени субъекта и длины (в битах) ключа.
ms.assetid: ee290c78-dbfa-4414-8489-aa886360652b
title: енроллсимплеусерцерт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0956455afa814af54cc86661f2d7733a6d16dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081014"
---
# <a name="enrollsimpleusercert"></a>енроллсимплеусерцерт

Пример Енроллсимплеусерцерт регистрирует конечного пользователя в центре сертификации (ЦС) с помощью шаблона, имени субъекта и длины ключа в битах.

## <a name="location"></a>Расположение

При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows устанавливается версия C++ образца по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллсимплеусерцерт. Версия C# установлена в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 Samples, посвященной \\ \\ регистрации сертификата X509 \\ \\ енроллсимплеусерцерт CSharp.

## <a name="discussion"></a>Разговор

Пример Енроллсимплеусерцерт:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать имя шаблона, имя субъекта и длину ключа.
2.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и инициализирует его с помощью шаблона.
3.  Извлекает объект запроса внутреннего сертификата из объекта регистрации и запрашивает его для объекта [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) . Самый внутренний запрос всегда является \# запросом PKCS 10.
4.  Извлекает объект [**IX509PrivateKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey) из \# запроса PKCS 10 и задает длину ключа, указанную в командной строке.
5.  Создает объект [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) , использует его для кодирования имени субъекта X. 500 и добавляет имя в \# запрос PKCS 10.
6.  Пытается зарегистрировать конечного пользователя в центре сертификации и отслеживать ход процесса регистрации. Функция Чеккенроллстатус определена в Енроллкоммон. cpp.

## <a name="related-topics"></a>См. также

<dl> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 



