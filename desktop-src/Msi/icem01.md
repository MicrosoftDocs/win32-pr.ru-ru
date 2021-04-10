---
description: ICEM01 проверяет работоспособность механизма ICE. В этом ICE для получения времени используется свойство Time, которое возвращает либо системное время, либо значение None.
ms.assetid: f3b7677d-6b2e-4aa0-92eb-1b1e62cdf0a6
title: ICEM01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca7f2ffb3fcf5e3d50a3937a1f17fddd3a912f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154806"
---
# <a name="icem01"></a>ICEM01

ICEM01 проверяет работоспособность механизма ICE. В этом ICE для получения времени используется свойство [**time**](time.md) , которое возвращает либо системное время, либо значение None.

Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.

## <a name="result"></a>Результат

ICEM01 отправляет сообщение, предоставляющее время, которое программа установки вызвала ICEM01. Эта ICE никогда не должна возвращать ошибку.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



