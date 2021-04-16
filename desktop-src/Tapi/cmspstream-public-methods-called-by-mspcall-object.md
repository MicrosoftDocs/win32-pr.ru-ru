---
description: В следующем списке содержатся методы Кмспстреам, вызываемые объектом Мспкалл.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Методы Кмспстреам, вызываемые объектом Мспкалл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683796"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>Кмспстреам открытые методы, вызываемые объектом Мспкалл



| Кмспстреам открытые методы                                 | Описание                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Ini**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Вызывается **мспкалл** при создании потока.                                   |
| [**Закрытия**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Вызывается методом **мспкалл** для отмены выбора всех объектов терминала и освобождения объекта вызова. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Вызывается объектом Мспкалл для получения текущего состояния потока.                   |
| [**хандлетспдата**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | Производный объект call может вызвать этот метод, чтобы поток мог выполнять команды TSP.     |
| [**процессграфевент**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Вызывается объектом Мспкалл, чтобы позволить потоку выполнять события графа.                     |



 

 

 



