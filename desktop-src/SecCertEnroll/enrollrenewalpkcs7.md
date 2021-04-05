---
description: Создает \# объект запроса PKCS 7 для продления существующего сертификата. Объект запроса использует новую пару ключей, но удерживает поставщик служб шифрования, связанный с обновляемым сертификатом.
ms.assetid: 12a3f1b4-b31e-470e-8ce6-87f497841240
title: enrollRenewalPKCS7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8795758a2744dcee07a100f87eb1db0a1af49eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545879"
---
# <a name="enrollrenewalpkcs7"></a>enrollRenewalPKCS7

Пример enrollRenewalPKCS7 создает \# объект запроса PKCS 7 для продления существующего сертификата. Объект запроса использует новую пару ключей, но удерживает поставщик служб шифрования, связанный с обновляемым сертификатом.

## <a name="location"></a>Расположение

При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ enrollRenewalPKCS7.

## <a name="discussion"></a>Разговор

Пример enrollRenewalPKCS7:

1.  Обрабатывает аргументы командной строки. Командная строка должна содержать имя шаблона, используемого для создания запроса на сертификат.
2.  Извлекает существующий сертификат с использованием имени шаблона, указанного в командной строке, или, если сертификат не найден, пытается зарегистрировать его с помощью шаблона. Функции Финдцертбитемплате и Енроллцертбитемплате определены в Енроллкоммон. cpp.
3.  Проверяет цепочку сертификатов и преобразует сертификат в **BSTR**.
4.  Создает объект [**IX509CertificateRequestPkcs7**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs7) и инициализирует его с помощью существующего сертификата. Поскольку параметр *инхеритоптионс* имеет значение инхеритдефаулт, для запроса создается новая пара ключей, но используется поставщик служб шифрования в существующем сертификате. Дополнительные сведения см. в описании метода [**инитиализефромцертификате**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509certificaterequestpkcs7-initializefromcertificate) .
5.  Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) , инициализирует его с помощью \# объекта запроса PKCS 7, пытается зарегистрировать его в центре сертификации и отслеживает состояние процесса регистрации. Функция Чеккенроллстатус определена в Енроллкоммон. cpp.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запрос CMC](cmc-request.md)
</dt> <dt>

[\#Запрос на продление PKCS 7](pkcs--7--renewal-request.md)
</dt> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

 



