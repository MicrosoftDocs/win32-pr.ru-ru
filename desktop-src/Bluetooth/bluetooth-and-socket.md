---
title: Bluetooth и сокет
description: Создает сокет для входящих или исходящих соединений.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Bluetooth сокета
- Bluetooth Bluetooth и сокетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004304"
---
# <a name="bluetooth-and-socket"></a>Bluetooth и сокет

Функция [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) создает сокет для входящих или исходящих соединений.

чтобы создать сокет с помощью Bluetooth, используйте следующие параметры:

-   параметр *af* функции [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) всегда имеет значение **af \_ бс** для сокетов Bluetooth.
-   Параметр *типа* функции [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) всегда **Сокк \_ Stream**; **Сокк \_** Сокеты дграм не поддерживаются Bluetooth.
-   Для параметра *протокола* **бспрото \_ RFCOMM** является поддерживаемым протоколом.

дополнительные сведения см. в разделе [сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**фиксатор**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 