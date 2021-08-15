---
description: Использование \_ \_ командного кода для обратной передачи SIO MultiPoint для включения или отключения замыкания на себя трафика MultiPoint.
ms.assetid: 7e11932b-ce9a-4500-888f-8a08ab67b46c
title: SIO_MULTIPOINT_LOOPBACK ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b75c781aeeaa67327dd2eaa57efb1eaccaf5d1d62daf3ffa9de3ce63fedbe2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097514"
---
# <a name="sio_multipoint_loopback-ioctl"></a>\_Ioctl MULTIPOINT с \_ замыканием на себя

При \_ использовании d конечных сокетов в некорневой плоскости данных, как правило, желательно иметь возможность контролировать, будет ли отправленный трафик также получен обратно на тот же сокет. Для \_ \_ включения или отключения замыкания на себя трафика MultiPoint используется код команды замыкания на себя для [**вспиоктл**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) .

 

 
