---
title: Bluetooth и прослушивание, выбор и функции closesocket
description: Bluetooth использует функции listen, select и функции closesocket без каких бы то ни было изменений в стандартном программировании Windowsных сокетов.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- функции closesocket
- прослушивание
- select
- Bluetooth и прослушивание
- Bluetooth и прослушивание выберите
- Bluetooth и прослушивание, выбор и функции closesocket
- прослушивание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fa3fc1285a9035173da80cc7a9821535409b872b171f7822708c379ff01543
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004484"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a>Bluetooth и прослушивание, выбор и функции closesocket

Bluetooth использует функции [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)и [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) без каких бы то ни было изменений в стандартном программировании Windowsных сокетов.

как и в случае с Windows сокетами, функция [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) освобождает ресурсы, связанные с сокетом.

При вызове функции [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) настоятельно рекомендуется использовать низкое значение для параметра *невыполненной работы* (обычно от 2 до 4), поскольку принимаются только несколько клиентских подключений. Это сокращает количество системных ресурсов, выделенных для использования сокетом прослушивания.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**слушивают**](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[**метьте**](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 