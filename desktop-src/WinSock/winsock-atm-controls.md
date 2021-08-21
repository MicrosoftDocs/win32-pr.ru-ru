---
description: установка и уничтожение подключений "точка — точка" и "точка — multipoint" изначально поддерживается спецификацией Windows sockets 2.
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Элементы управления Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed891f24c16f01025d0bd06da1ea3ec9c0cca01abdcaf3c9950229bf512f0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051452"
---
# <a name="winsock-atm-controls"></a>Элементы управления Winsock ATM

установка и уничтожение подключений "точка — точка" и "точка — multipoint" изначально поддерживается спецификацией Windows sockets 2. на самом деле, спецификации качества обслуживания сокетов 2 Windows и независимые от протокола механизмы multipoint и многоадресной рассылки разрабатывались с учетом банкоматов вместе с другими протоколами. см. раздел 2,7 и приложение D спецификации API Windows sockets 2 для Windows сокетов 2, качества обслуживания и поддержки Multipoint соответственно. Поэтому в этом документе не нужно вводить запросы ioctl, относящиеся к ATM.

 

 



