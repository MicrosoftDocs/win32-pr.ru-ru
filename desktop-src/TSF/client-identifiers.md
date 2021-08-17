---
title: Идентификаторы клиентов
description: Идентификаторы клиентов
ms.assetid: 69ff159c-9264-4958-a712-4aa50db6e48e
keywords:
- Платформа текстовых служб (TSF), идентификаторы клиентов
- TSF (платформа текстовых служб), идентификаторы клиентов
- текстовые службы, идентификаторы клиентов
- Приложения с поддержкой TSF, идентификаторы клиентов
- идентификаторы клиентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f37b230eed1f47ad3e31a5831bddaf8634837c1173806deb084c1e3a4d08790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953912"
---
# <a name="client-identifiers"></a>Идентификаторы клиентов

## <a name="applications"></a>Приложения

Приложение получает свой идентификатор клиента путем вызова [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).

## <a name="text-services"></a>Текстовые службы

Служба текстового ввода получает свой идентификатор клиента при вызове метода [итфтекстинпутпроцессор:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) текстовой службы.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> <dt>

[Итфтекстинпутпроцессор:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> </dl>

 

 




