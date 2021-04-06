---
description: Следующие свойства определяются интерфейсом Ицертсрвсетупкэйинформатион.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Свойства Ицертсрвсетупкэйинформатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910072"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a>Свойства Ицертсрвсетупкэйинформатион

Следующие свойства определяются интерфейсом [**ицертсрвсетупкэйинформатион**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .



| Свойство                                                                           | Описание                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContainerName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | Возвращает или задает имя, используемое [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для создания, хранения ключа или доступа к нему.                                                                       |
| [**Существующий**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | Возвращает или задает значение, указывающее, существует ли уже закрытый ключ.                                                                                                                                                                                                                       |
| [**ексистингкацертификате**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | Возвращает или задает двоичное значение, закодированное с помощью [*distinguished Encoding Rules*](../secgloss/d-gly.md) (Der) и представляющее собой двоичное значение сертификата ЦС, соответствующего существующему ключу. |
| [**HashAlgorithm**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | Возвращает или задает имя хэш-алгоритма, используемого для подписания или проверки сертификата ЦС для ключа.                                                                                                                                                                                                |
| [**Длина**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | Возвращает или задает стойкость ключа к одному из значений, поддерживаемых CSP.                                                                                                                                                                                                                   |
| [**ProviderName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | Возвращает или задает имя CSP, используемого для создания или хранения закрытого ключа.                                                                                                                                                                                                               |



 

 

 
