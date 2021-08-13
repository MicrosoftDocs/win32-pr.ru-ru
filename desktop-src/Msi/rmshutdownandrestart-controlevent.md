---
description: уведомляет установщик Windows использовать диспетчер перезапуска для завершения работы всех приложений, в которых используются файлы, и для их перезапуска в конце установки.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: Рмшутдовнандрестарт таблице ControlEvent событие
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f483e485eeefc2d3a761a3d9c9ff95989a3150dcfd8fff6a36bfb6211504e95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625894"
---
# <a name="rmshutdownandrestart-controlevent"></a>Рмшутдовнандрестарт таблице ControlEvent событие

это событие уведомляет установщик Windows использовать [диспетчер перезапуска](../rstmgr/restart-manager-portal.md) для завершения работы всех приложений, в которых используются файлы, и для их перезапуска в конце установки.

Этот таблице ControlEvent событие не действует, если выполняется одно из следующих условий.

-   операционная система, на которой работает установка, не Windows Vista или Windows Server 2008.
-   Взаимодействие с [диспетчером перезапуска](../rstmgr/restart-manager-portal.md) отключено свойством [**Мсирестартманажерконтрол**](msirestartmanagercontrol.md) или политикой [дисаблеаутоматикаппликатионшутдовн](disableautomaticapplicationshutdown.md) .
-   В настоящее время нет открытого сеанса [диспетчера перезапуска](../rstmgr/restart-manager-portal.md) .
-   любые вызовы установщик Windows в [диспетчер перезапуска](../rstmgr/restart-manager-portal.md) возвращают ошибку.

## <a name="typical-use"></a>Типичные случаи использования

Событие элемента управления Рмшутдовнандрестарт публикуется только в элементе управления " [кнопка](pushbutton-control.md) " в [диалоговом окне мсирмфилесинусе](msirmfilesinuse-dialog.md) .

 

 
