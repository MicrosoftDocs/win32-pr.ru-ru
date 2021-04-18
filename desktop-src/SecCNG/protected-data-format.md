---
description: Защищенные данные хранятся в виде большого двоичного объекта в кодировке ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Формат защищенных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156146"
---
# <a name="protected-data-format"></a>Формат защищенных данных

Защищенные данные хранятся в виде большого двоичного объекта в кодировке ASN. 1. Данные форматируются как CMS (синтаксис сообщений сертификата) в виде упакованного содержимого. Цифровой конверт содержит зашифрованное содержимое, сведения о получателе, содержащие зашифрованный ключ шифрования содержимого (CEK), и заголовок, содержащий сведения о содержимом, включая строку правила незашифрованного дескриптора защиты. Это показано на следующей схеме.

![защищенные запечатанные данные](images/protecteddatablob.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Дескрипторы защиты](protection-descriptors.md)
</dt> <dt>

[Поставщики защиты](protection-providers.md)
</dt> </dl>

 

 



