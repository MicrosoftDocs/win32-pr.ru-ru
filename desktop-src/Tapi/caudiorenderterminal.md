---
description: Терминал Каудиорендертерминал является производным от Ксинглефилтертерминал и реализует статический терминал воспроизведения звука для звуковых устройств с помощью фильтра звука DirectShow. Большинству MSP не требуется переопределять реализацию этого терминала.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: каудиорендертерминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683797"
---
# <a name="caudiorenderterminal"></a>каудиорендертерминал

Терминал **каудиорендертерминал** является производным от [ксинглефилтертерминал](csinglefilterterminal.md) и реализует статический терминал воспроизведения звука для звуковых устройств с помощью фильтра звука DirectShow. Большинству MSP не требуется переопределять реализацию этого терминала.

Определен в Мсптрмар. h.

## <a name="remarks"></a>Комментарии

Методы [**помещения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) и [**получения \_ баланса**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) **каудиорендертерминал** не реализованы и будут возвращать E \_ нотимпл.

 

 



