---
description: Поставщик служб шифрования Microsoft RSA/SChannel поддерживает хеширование, подписывание данных и проверку подписей.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Поставщик служб шифрования Microsoft RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b38ef6573cada965c0b5e982d7808a7fe2b7670271f4f8ce1fd51c99d002db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100694"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Поставщик служб шифрования Microsoft RSA/SChannel

Поставщик криптографии Microsoft [*RSA*](../secgloss/r-gly.md) / [*SChannel*](../secgloss/s-gly.md) поддерживает хеширование, подписывание данных и проверку подписей. Идентификатор алгоритма КАЛГ \_ SSL3 \_ SHAMD5 используется для проверки подлинности клиента SSL 3,0 и TLS 1,0. Этот CSP поддерживает получение ключей для протоколов SSL2, PCT1, SSL3 и TLS1. [*Хэш*](../secgloss/h-gly.md) состоит из объединения хэша MD5 с хэшем SHA и подписанного [*закрытым ключом*](../secgloss/p-gly.md)RSA. Его можно экспортировать в другие страны и регионы.



|                   | Значение                         |
|-------------------|-------------------------------|
| **Тип поставщика** | PROV \_ RSA \_ SChannel           |
| **Имя поставщика** | MS \_ DEF \_ RSA \_ SChannel \_ Prov  |



 

Дополнительные сведения о поставщиках RSA/SChannel см. в разделе [функции CSP](cryptography-functions.md).

 

 
