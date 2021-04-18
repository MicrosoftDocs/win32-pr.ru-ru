---
description: Поток может в любой момент вызвать Всаисблоккинг, чтобы определить, выполняется ли в данный момент блокирующий вызов.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Отмена блокирующих операций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701555"
---
# <a name="canceling-blocking-operations"></a>Отмена блокирующих операций

Поток может в любой момент вызвать [всаисблоккинг](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) , чтобы определить, выполняется ли в данный момент блокирующий вызов. (Эта функция реализована в оболочках совместимости Windows Sockets 1,1 и, следовательно, не имеет аналога SPI.) Очевидно, что это возможно только в том случае, если псевдо-блокировка используется поставщиком услуг. При необходимости [**вспканцелблоккингкалл**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) может быть вызван в любое время для отмены любой текущей операции псевдо.

 

 
