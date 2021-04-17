---
title: СторахЦи заменяет МСАХЦИ
description: СторахЦи заменяет МСАХЦИ
ms.assetid: 9C6FAFA7-A6B3-4D3A-94EE-B53626DBF183
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a41a9b113ba33c35e3a1a1c4b2ea5dad3054c8
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "105700961"
---
# <a name="storahci-replaces-msahci"></a>СторахЦи заменяет МСАХЦИ

## <a name="platforms"></a>Платформы

**Клиенты** — Windows 8  
**Серверы** — Windows Server 2012  


## <a name="description"></a>Описание

СторахЦи, Минипорт Storport, поддерживает контроллеры интерфейса AHCI с последовательным подключением (SATA) в Windows и заменяет МСАХЦИ, Мини-порт Атапорт.

## <a name="manifestation"></a>Проявление

В функциональности или производительности не должно быть изменений; Этот драйвер поддерживает все устройства, которые поддерживает МСАХЦИ.

Это изменение прозрачно для пользователя.

## <a name="mitigation"></a>Меры по снижению риска

Обновите все служебные программы и скрипты, использующие привязки Атапорт. Не полагайтесь на имя диска. Вместо этого используйте обнаружение дисков стандартного типа.

 

 




