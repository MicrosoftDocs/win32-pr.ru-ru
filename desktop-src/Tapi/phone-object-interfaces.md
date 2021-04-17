---
description: Объект Phone — это сущность, представляющая реальное телефонное устройство и все его элементы управления.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Интерфейсы объекта Phone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683909"
---
# <a name="phone-object-interfaces"></a>Интерфейсы объекта Phone

Объект Phone — это сущность, представляющая реальное телефонное устройство и все его элементы управления.

Интерфейсы [**итфонивент**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) и [**иенумфоне**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) не предоставляются напрямую в объекте Phone, но тесно связаны с ним и перечислены здесь для удобства использования справки.



| Интерфейс                                                  | Описание                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | Разрешает доступ к телефонному устройству на уровне, сравнимом с интерфейсом TAPI 2. API *x* C.                                      |
| [**итаутоматедфонеконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | Предоставляет методы для автоматического управления тонами и кольцами телефона, а также для автоматизированной обработки вызовов на основе состояния хуксвитч телефона. |
| [**итфонивент**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | Извлекает описание событий телефона.                                                                                                |
| [**иенумфоне**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | Перечисляет [**итфоне**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).                                                                                                    |



 

 

 



