---
description: Объект InkOverlay можно присоединить к элементу управления "окно" и использовать для реализации базовой возможности рукописного ввода.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Стирание с помощью объекта InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf85926f3566340cbde0d3202f3485e7c54cccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810085"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Стирание с помощью объекта InkOverlay

Объект [**InkOverlay**](inkoverlay-class.md) можно присоединить к элементу управления "окно" и использовать для реализации базовой возможности рукописного ввода. Объект **InkOverlay** можно использовать для стирания рукописного ввода, установив свойство [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) равным **Delete**. Затем можно присвоить свойству [**ерасермоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) либо элемент **Stroke** , либо элемент **Point** объекта [**инковерлайерасермоде**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). Установка для свойства **ерасермоде** значения **Stroke** стирает все штрихи. Установка для свойства **ерасермоде** значения **Point** стирает перо, над которым проходит курсор.

 

 



