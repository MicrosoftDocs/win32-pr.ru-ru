---
description: WIA представляет устройство камеры в виде иерархического дерева объектов Ивиаитем.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Устройства камеры WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2023af90df6f868dfcace6f088bfe7ffeb6b549e0e20661231497f3fdf014
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592732"
---
# <a name="wia-camera-devices"></a>Устройства камеры WIA

WIA представляет устройство камеры в виде иерархического дерева объектов [**ивиаитем**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . корневой элемент, возвращенный из Windows вызова метода [**ивиадевмгр:: креатедевице**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) диспетчера устройств (WIA), используется для получения и задания сведений об устройстве, управления устройством и для начала перечисления элементов устройства.

> [!Note]  
> WIA не поддерживает камеры в Windows Vista и более поздних версиях. для этих версий Windows используйте API-интерфейс Windows Portable Device (WPD), описанный в пакете средств разработки драйверов Windows (DDK) для получения изображений из камер.

 

На следующей схеме показан пример реализации камеры. Корневой элемент камеры имеет три дочерних элемента: два изображения и одна папка. В папке есть два дочерних элемента, оба рисунка.

![Реализация образца камеры](images/wihierar.gif)

 

 



