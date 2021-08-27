---
description: Объект InkOverlay можно присоединить к элементу управления "окно" и использовать для реализации базовой возможности рукописного ввода.
ms.assetid: c15d80dc-0cbf-48a2-9f5d-d94d521b1a8c
title: Стирание с помощью объекта InkOverlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6d95e7939bc53c534d3bfc9a542e40b95fbce05234000e24b107f0f2625eae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110944"
---
# <a name="erasing-by-using-the-inkoverlay-object"></a>Стирание с помощью объекта InkOverlay

Объект [**InkOverlay**](inkoverlay-class.md) можно присоединить к элементу управления "окно" и использовать для реализации базовой возможности рукописного ввода. Объект **InkOverlay** можно использовать для стирания рукописного ввода, установив свойство [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) равным **Delete**. Затем можно присвоить свойству [**ерасермоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) либо элемент **Stroke** , либо элемент **Point** объекта [**инковерлайерасермоде**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode). Установка для свойства **ерасермоде** значения **Stroke** стирает все штрихи. Установка для свойства **ерасермоде** значения **Point** стирает перо, над которым проходит курсор.

 

 



