---
description: Создает пользовательский запрос PKCS \# 10 и пытается зарегистрировать его в центре сертификации (ЦС) предприятия.
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb88a2295217874a12da8b701a46f8dafe3db1cbf53d01273222e607195a789a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780043"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

Пример enrollCustomPKCS10 \_ 2 создает пользовательский \# запрос PKCS 10 и пытается зарегистрировать его в [*центре сертификации*](/windows/desktop/SecGloss/c-gly) (ЦС) предприятия.

## <a name="location"></a>Расположение

при установке пакета Microsoft Windows Software Development Kit (SDK) образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples Security ssl \\ \\ Certificate \\ \\ enrollCustomPKCS10 \_ 2.

## <a name="discussion"></a>Разговор

Пример enrollCustomPKCS10 \_ 2:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать имя шаблона и имя поставщика служб шифрования.
2.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и инициализирует его с помощью имени шаблона, указанного в командной строке.
3.  Получает [*запрос сертификата*](/windows/desktop/SecGloss/c-gly) из объекта регистрации.
4.  Извлекает \# из объекта запроса сертификата самый внутренний запрос PKCS 10, полученный на шаге 3.
5.  Извлекает [*закрытый ключ*](/windows/desktop/SecGloss/p-gly) из \# запроса PKCS 10.
6.  Создает коллекцию [**икспинформатионс**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) и добавляет доступные в нее поставщики служб шифрования, а затем извлекает объект [**икспстатус**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) для поставщика, указанного в командной строке.
7.  Задает объект состояния для закрытого ключа.
8.  Пытается зарегистрировать [*запрос на сертификат*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[\#Запрос PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 
