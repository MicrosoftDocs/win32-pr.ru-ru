---
description: Поставщики услуг, поддерживающие абстракцию внештатных данных (OOB) для сокетов в стиле потока, должны соответствовать семантике в этом разделе.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Данные по внештатному каналу в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741059"
---
# <a name="out-of-band-data-in-the-spi"></a>Данные по внештатному каналу в SPI

Поставщики услуг, поддерживающие абстракцию внештатных данных (OOB) для сокетов в стиле потока, должны соответствовать семантике в этом разделе. Мы будем описывать обработку данных OOB с помощью независимого от протокола способа. Сведения о данных OOB, реализованных с помощью срочных данных в поставщиках услуг TCP/IP, см. в этом [приложении](winsock-annexes.md) . В следующем примере использование [**вспрекв**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) также применяется к [**вспреквфром**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
