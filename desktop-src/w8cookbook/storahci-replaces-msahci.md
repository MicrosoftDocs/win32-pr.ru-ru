---
title: СторахЦи заменяет МСАХЦИ
description: СторахЦи заменяет МСАХЦИ
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6affffe41dd00c009ebb7bebf508dac1b63bec673c17783f594d22969822e542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932144"
---
# <a name="storahci-replaces-msahci"></a>СторахЦи заменяет МСАХЦИ

## <a name="platforms"></a>Платформы

**клиенты** — Windows 8  
**серверы** — Windows Server 2012  


## <a name="description"></a>Описание

сторахЦи, минипорт storport, поддерживает контроллеры AHCI с последовательным интерфейсом (SATA) в Windows и заменяет мсахЦи, мини-порт атапорт.

## <a name="manifestation"></a>Проявление

В функциональности или производительности не должно быть изменений; Этот драйвер поддерживает все устройства, которые поддерживает МСАХЦИ.

Это изменение прозрачно для пользователя.

## <a name="mitigation"></a>Меры по снижению риска

Обновите все служебные программы и скрипты, использующие привязки Атапорт. Не полагайтесь на имя диска. Вместо этого используйте обнаружение дисков стандартного типа.

 

 




