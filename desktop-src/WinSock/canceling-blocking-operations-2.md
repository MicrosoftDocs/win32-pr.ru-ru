---
description: Поток может в любой момент вызвать Всаисблоккинг, чтобы определить, выполняется ли в данный момент блокирующий вызов.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Отмена блокирующих операций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030694"
---
# <a name="canceling-blocking-operations"></a>Отмена блокирующих операций

Поток может в любой момент вызвать [всаисблоккинг](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) , чтобы определить, выполняется ли в данный момент блокирующий вызов. (эта функция реализована в оболочках совместимости Windows sockets 1,1 и, следовательно, не имеет аналога SPI.) Очевидно, что это возможно только в том случае, если псевдо-блокировка используется поставщиком услуг. При необходимости [**вспканцелблоккингкалл**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) может быть вызван в любое время для отмены любой текущей операции псевдо.

 

 
