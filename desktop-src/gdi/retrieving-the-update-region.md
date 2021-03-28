---
description: Функции Жетупдатерект и Жетупдатергн извлекают текущий регион обновления для окна.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Получение региона обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263651"
---
# <a name="retrieving-the-update-region"></a>Получение региона обновления

Функции [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) и [**жетупдатергн**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) извлекают текущий регион обновления для окна. Жетупдатерект извлекает наименьший прямоугольник (в логических координатах), охватывающий всю область обновления. Жетупдатергн извлекает сам регион обновления. Эти функции можно использовать для вычисления текущего размера области обновления, чтобы определить, где нужно выполнить операцию рисования.

[**Бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) также получает размеры самого маленького прямоугольника, охватывающего текущую область обновления, копируя измерения в элемент **члене rcpaint структуры** в структуре [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) . Так как **бегинпаинт** проверяет регион обновления, любой вызов [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) и [**жетупдатергн**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) сразу после вызова **бегинпаинт** возвращает пустой регион обновления.

 

 



