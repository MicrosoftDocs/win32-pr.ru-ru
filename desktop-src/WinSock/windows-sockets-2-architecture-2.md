---
description: Архитектура Windows Sockets 2 (Winsock) совместима с архитектурой Windows Open System (ВОСА).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Архитектура Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155262"
---
# <a name="windows-sockets-2-architecture"></a>Архитектура Windows Sockets 2

Архитектура Windows Sockets 2 совместима с архитектурой Windows Open System (ВОСА), как показано ниже:

![Архитектура Windows Sockets 2](images/ovrvw2-1.png)

Winsock определяет стандартный интерфейс поставщика услуг (SPI) между прикладным программным интерфейсом (API) и его функциями, экспортированными из WS2 \_32.dll и стеками протоколов. Следовательно, поддержка Winsock не ограничена протоколами TCP/IP, как в случае с сокетами Windows 1,1.

Архитектура Windows Sockets 2 не является обязательной или желательной, чтобы поставщики стеков предWS2и собственную реализацию \_32.dll, поскольку один WS2 \_32.dll должен работать во всех стеках. WS2 \_32.dll и оболочки совместимости должны быть просмотрены так же, как компонент операционной системы.

 

 



