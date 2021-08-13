---
description: Защищенные данные хранятся в виде большого двоичного объекта в кодировке ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Формат защищенных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b4985fee02b5c40b9ad51a6645c4e0d9894a358a871c2067e44dd5f90da26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907414"
---
# <a name="protected-data-format"></a>Формат защищенных данных

Защищенные данные хранятся в виде большого двоичного объекта в кодировке ASN. 1. Данные форматируются как CMS (синтаксис сообщений сертификата) в виде упакованного содержимого. Цифровой конверт содержит зашифрованное содержимое, сведения о получателе, содержащие зашифрованный ключ шифрования содержимого (CEK), и заголовок, содержащий сведения о содержимом, включая строку правила незашифрованного дескриптора защиты. Это показано на следующей схеме.

![защищенные запечатанные данные](images/protecteddatablob.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Дескрипторы защиты](protection-descriptors.md)
</dt> <dt>

[Поставщики защиты](protection-providers.md)
</dt> </dl>

 

 



