---
description: Исходный базовый поставщик неправильно сообщил о том, что хэш-алгоритм SHA перечислит алгоритмы, выполнив вызовы Криптжетпровпарам с параметром PP \_ енумалгс.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Функциональность SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808320"
---
# <a name="sha-functionality"></a>Функциональность SHA

Исходный базовый поставщик неправильно сообщил о том, что хэш-алгоритм [*SHA*](../secgloss/s-gly.md) перечислит алгоритмы, выполнив вызовы [**криптжетпровпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) с параметром PP \_ енумалгс. Это было исправлено в базовом поставщике. Измененный базовый поставщик и расширенный поставщик, и теперь правильно сообщает о SHA-1.

В \_ винкрипт. h была добавлена определенная константа SHA1 калг с тем же значением, что и в калг \_ SHA.

 

 
