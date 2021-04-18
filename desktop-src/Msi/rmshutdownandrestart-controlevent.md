---
description: Уведомляет установщик Windows использовать диспетчер перезапуска для завершения работы всех приложений, в которых используются файлы, и для их перезапуска в конце установки.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: Рмшутдовнандрестарт таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650633"
---
# <a name="rmshutdownandrestart-controlevent"></a>Рмшутдовнандрестарт таблице ControlEvent событие

Это событие уведомляет установщик Windows использовать [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) для завершения работы всех приложений, в которых используются файлы, и для их перезапуска в конце установки.

Этот таблице ControlEvent событие не действует, если выполняется одно из следующих условий.

-   Операционной системой, в которой работает установка, не является Windows Vista или Windows Server 2008.
-   Взаимодействие с [диспетчером перезапуска](../rstmgr/restart-manager-portal.md) отключено свойством [**Мсирестартманажерконтрол**](msirestartmanagercontrol.md) или политикой [дисаблеаутоматикаппликатионшутдовн](disableautomaticapplicationshutdown.md) .
-   В настоящее время нет открытого сеанса [диспетчера перезапуска](../rstmgr/restart-manager-portal.md) .
-   Любые вызовы установщик Windows в [Диспетчер перезапуска](../rstmgr/restart-manager-portal.md) возвращают ошибку.

## <a name="typical-use"></a>Типичные случаи использования

Событие элемента управления Рмшутдовнандрестарт публикуется только в элементе управления " [кнопка](pushbutton-control.md) " в [диалоговом окне мсирмфилесинусе](msirmfilesinuse-dialog.md) .

 

 
