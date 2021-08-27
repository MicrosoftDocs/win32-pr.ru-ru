---
description: организация пространства имен в Windows сокетах (Winsock) SPI.
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: Организация пространства имен в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d3cd2569f90009ceb4db9ceaca3d5020c6949e7e69842b96030cab4634c534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121384"
---
# <a name="namespace-organization-in-the-spi"></a>Организация пространства имен в SPI

Многие пространства имен упорядочиваются иерархически. Некоторые, такие как X. 500 и NDS, разрешают неограниченное вложение. Другие позволяют объединять службы в один уровень иерархии или группы. Обычно это называется рабочей группой. При создании запроса часто бывает необходимо установить контекстную точку внутри иерархии пространства имен, из которой начнется поиск.

 

 



