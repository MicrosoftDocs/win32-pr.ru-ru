---
description: эллиптические кривые включены в Windows 10 версий 1507 и 1511.
title: эллиптические кривые TLS в Windows 10 версии 1507 и 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 91dfc7dac8f45b9c4f2231f6db93e776c75544373199170146f55362f02f2be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915869"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>эллиптические кривые TLS в Windows 10 версии 1507 и 1511

для Windows 10 версии 1507 и 1511 следующие эллиптические кривые по умолчанию включены и по этому приоритету используют поставщик Microsoft Schannel:

| Строка эллиптической кривой | Доступно в режиме FIPS |
|-------------|--------------|
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
- чтобы использовать групповую политику, [настройте порядок кривых ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) в разделе конфигурация компьютера > административные шаблоны > сеть > конфигурация SSL Параметры с списком приоритет для всех включенных эллиптических кривых.

- Чтобы использовать PowerShell, ознакомьтесь с [командлетами TLS](/powershell/module/tls) , чтобы получить полный список синтаксиса и описаний командлетов TLS.


> [!NOTE]
> до Windows 10 строки набора шифров добавляются с эллиптической кривой для определения приоритета кривой. Windows 10 поддерживает настройку порядка приоритета эллиптической кривой, поэтому суффикс эллиптической кривой не является обязательным и переопределяется новым порядковым приоритетом эллиптической кривой, когда он предоставляется, чтобы разрешить организациям использовать групповую политику для настройки различных версий Windows с одинаковыми комплектами шифров.


## <a name="see-also"></a>См. также

[Настройка порядка кривых ECC TLS](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Управление порядком TLS ECC](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[управление кривыми Windows ECC с помощью групповая политика](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Командлеты TLS](/powershell/module/tls)
