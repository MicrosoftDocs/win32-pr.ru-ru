---
description: Терминал Каудиокаптуретерминал является производным от Ксинглефилтертерминал и реализует статический терминал аудио-захвата для звуковых устройств с помощью фильтра Wave. Большинству MSP не требуется переопределять реализацию этого терминала.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: каудиокаптуретерминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674023"
---
# <a name="caudiocaptureterminal"></a>каудиокаптуретерминал

Терминал **каудиокаптуретерминал** является производным от [ксинглефилтертерминал](csinglefilterterminal.md) и реализует статический терминал аудио-захвата для звуковых устройств с помощью фильтра Wave. Большинству MSP не требуется переопределять реализацию этого терминала.

Определен в Мсптмак. h.

## <a name="remarks"></a>Комментарии

Методы [**помещения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) и [**получения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) **каудиокаптуретерминал** не реализованы и будут возвращать E \_ нотимпл.

 

 



