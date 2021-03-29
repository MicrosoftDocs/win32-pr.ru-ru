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
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792421"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth и жетсоккопт

Bluetooth использует функцию [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) для запроса различных параметров, связанных с каналом сервера или соединением. Использование **жетсоккопт** с Bluetooth имеет следующие требования.

-   Параметр *s* параметра [**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt) должен быть допустимым сокетом Bluetooth.
-   Параметр *Level* параметра [**ЖЕТСОККОПТ**](/windows/desktop/api/winsock/nf-winsock-getsockopt) должен быть Sol \_ RFCOMM.

Список доступных параметров сокетов Bluetooth см. в разделе [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**жетсоккопт**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 