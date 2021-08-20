---
title: Bluetooth и жетсоккопт
description: Bluetooth использует функцию жетсоккопт для запроса различных параметров, связанных с каналом сервера или соединением.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- жетсоккопт
- Bluetooth и жетсоккопт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee63d8dc1665868023967dd88c5ba223cce538c1fa1d41dd151329f6bf52f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081088"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth и жетсоккопт

Bluetooth использует функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) для запроса различных параметров, связанных с каналом сервера или соединением. использование **жетсоккопт** с Bluetooth имеет следующие требования.

-   параметр *s* параметра [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) должен быть допустимым сокетом Bluetooth.
-   Параметр *Level* параметра [**ЖЕТСОККОПТ**](/windows/desktop/api/winsock/nf-winsock-getsockopt) должен быть Sol \_ RFCOMM.

список доступных параметров сокета Bluetooth см. в разделе [Bluetooth и параметры сокета](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 