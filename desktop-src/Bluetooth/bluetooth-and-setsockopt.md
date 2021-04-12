---
title: Bluetooth и сетсоккопт
description: Bluetooth использует функцию сетсоккопт для установки различных параметров, связанных с каналом сервера или соединением.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- сетсоккопт
- Bluetooth и сетсоккопт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337753"
---
# <a name="bluetooth-and-setsockopt"></a>Bluetooth и сетсоккопт

Bluetooth использует функцию [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для установки различных параметров, связанных с каналом сервера или соединением. Использование **сетсоккопт** с Bluetooth имеет следующие требования.

-   Параметр *s* параметра [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должен быть допустимым сокетом Bluetooth.
-   Параметр *Level* параметра [**СЕТСОККОПТ**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должен быть Sol \_ RFCOMM.

Список доступных параметров сокетов Bluetooth см. в разделе [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 