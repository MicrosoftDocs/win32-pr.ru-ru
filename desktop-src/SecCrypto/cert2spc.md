---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664841"
---
# <a name="cert2spc"></a>Cert2SPC

Средство Cert2SPC создает тестовый [*сертификат издателя программного обеспечения*](../secgloss/s-gly.md) (SPC) с помощью существующих [*сертификатов*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) . Cert2SPC может заключить несколько сертификатов X. 509 в объект данных, подписанных [*PKCS \# 7*](../secgloss/p-gly.md) . Средство устанавливается в \\ папку bin пути установки пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.

Cert2SPC доступен в составе Windows SDK, который можно скачать из <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Это средство предназначено только для тестирования. Допустимый SPC получен из [*центра сертификации*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1. cer Cert2. cer* ... *Output. SPC*

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Имена сертификатов X. 509 для включения в SPC. Каждое имя сертификата заканчивается расширением CER.                         |
| *Output. SPC*            | Имя \# объекта PKCS 7, содержащего создаваемые сертификаты X. 509. Имя выходного файла заканчивается расширением SPC. |



 

 

 
