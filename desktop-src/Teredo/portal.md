---
title: Протокол Teredo
description: Протокол Teredo
ms.assetid: fc213675-dbdb-42a1-a09f-dda598b95b94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946932d7a699a4e9b993ed93e8d48faafbd75fbb0ec54e61b260b8a25e634ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354467"
---
# <a name="teredo"></a>Протокол Teredo

## <a name="purpose"></a>Назначение

Teredo — это технология туннелирования IPv6, которая обеспечивает назначение адресов и автоматическое туннелирование между узлами для одноадресного трафика IPv6, когда узлы IPv6 и IPv4 находятся за одним или несколькими трансляторами сетевых адресов (NAT) IPv4. Для обхода NAT протоколов IPv4 пакеты IPv6 отправляются в виде сообщений UDP.

## <a name="developer-audience"></a>Аудитория разработчиков

Teredo предназначен для использования разработчиками C/C++ с возможностями сетевого программирования IPv6.

## <a name="run-time-requirements"></a>Требования к среде выполнения

интерфейс Teredo в основном поддерживается Windows Vista и Windows Server 2008. ограниченная функциональность интерфейса teredo, поддерживаемого Windows XP с пакетом обновления 2 (sp2) и Windows Server 2003, подробно описана в разделе [получение запрошенного трафика через Teredo](receiving-solicited-traffic-over-teredo.md).

## <a name="in-this-section"></a>В этом разделе



| Раздел                                       | Описание                                                                                |
|---------------------------------------------|--------------------------------------------------------------------------------------------|
| [О Teredo](about-teredo.md)<br/> | Сведения об интерфейсе Teredo.<br/>                                         |
| [Использование Teredo](using-teredo.md)<br/> | Сведения о реализации и общем использовании интерфейса Teredo.<br/> |



 

 

 





