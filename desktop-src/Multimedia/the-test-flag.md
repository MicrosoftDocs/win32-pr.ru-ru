---
title: Флаг теста
description: Флаг теста
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Флаг MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801483"
---
# <a name="the-test-flag"></a>Флаг теста

Флаг Test ( \_ тест MCI) выполняет запрос устройства, чтобы определить, может ли он выполнить команду. Устройство возвращает ошибку, если не может выполнить команду. Он не возвращает ошибку, если может справиться с командой. При указании этого флага MCI возвращает управление приложению, не выполняя команду.

Этот флаг поддерживается устройствами цифрового видео и ВИДЕОМАГНИТОФОНА для всех команд, кроме [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) и [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)).

 

 




