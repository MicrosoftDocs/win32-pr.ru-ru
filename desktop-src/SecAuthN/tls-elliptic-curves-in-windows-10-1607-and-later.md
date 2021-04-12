---
description: Эллиптические кривые включены в Windows 10 версии 1607 и более поздних.
title: Эллиптические кривые TLS в Windows 10 версии 1607 и более поздних
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265928"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Эллиптические кривые TLS в Windows 10 версии 1607 и более поздних

Для Windows 10, 1607 и более поздних версий, следующие эллиптические кривые включены и по умолчанию используют поставщик Schannel (Майкрософт) в этом порядке приоритета:

| Строка эллиптической кривой | Доступно в режиме FIPS |
|-------------|--------------|
| curve25519 | Нет |
| NistP256 | Да |
| NistP384 | Да |


Следующие эллиптические кривые поддерживаются поставщиком Schannel (Майкрософт), но не включены по умолчанию.

| Строка эллиптической кривой | Доступно в режиме FIPS |
|-------------|--------------|
| brainpoolP256r1 | Нет |
| brainpoolP384r1 | Нет |
| brainpoolP512r1 | Нет |
| nistP192 | Нет |
| nistP224 | Нет |
| nistP521 | Да |
| secP160k1 | Нет |
| secP160r1 | Нет |
| secP160r2 | Нет |
| secP192k1 | Нет |
| secP192r1 | Нет |
| secP224k1 | Нет |
| secP224r1 | Нет |
| secP256k1 | Нет |
| secP256r1 | Нет |
| secP384r1 | Нет |
| secP521r1 | Нет |



## <a name="enabling-elliptic-curves"></a>Включение эллиптических кривых

Чтобы добавить эллиптические кривые, разверните групповую политику или используйте командлеты TLS.
- Чтобы использовать групповую политику, [Настройте порядок КРИВЫХ ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) в разделе конфигурация компьютера > административные шаблоны > параметры конфигурации сети > SSL с списком приоритет для всех включенных эллиптических кривых.

- Чтобы использовать PowerShell, ознакомьтесь с [командлетами TLS](/powershell/module/tls) , чтобы получить полный список синтаксиса и описаний командлетов TLS.


> [!NOTE]
> До Windows 10 строки комплекта шифров были добавлены с эллиптической кривой для определения приоритета кривой. Windows 10 поддерживает настройку порядка приоритетов на основе эллиптических кривых, поэтому суффикс эллиптической кривой не является обязательным и переопределяется новым порядковым приоритетом эллиптической кривой, когда он предоставляется, чтобы разрешить организациям использовать групповую политику для настройки различных версий Windows с одинаковыми комплектами шифров.


## <a name="see-also"></a>См. также:

[Настройка порядка кривых ECC TLS](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Управление порядком TLS ECC](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Управление кривыми ECC Windows с помощью групповая политика](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Командлеты TLS](/powershell/module/tls)
