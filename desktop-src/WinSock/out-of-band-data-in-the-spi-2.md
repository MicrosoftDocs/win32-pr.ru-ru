---
description: Поставщики услуг, поддерживающие абстракцию внештатных данных (OOB) для сокетов в стиле потока, должны соответствовать семантике в этом разделе.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Данные по внештатному каналу в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072739"
---
# <a name="out-of-band-data-in-the-spi"></a>Данные по внештатному каналу в SPI

Поставщики услуг, поддерживающие абстракцию внештатных данных (OOB) для сокетов в стиле потока, должны соответствовать семантике в этом разделе. Мы будем описывать обработку данных OOB с помощью независимого от протокола способа. Сведения о данных OOB, реализованных с помощью срочных данных в поставщиках услуг TCP/IP, см. в этом [приложении](winsock-annexes.md) . В следующем примере использование [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) также применяется к [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
