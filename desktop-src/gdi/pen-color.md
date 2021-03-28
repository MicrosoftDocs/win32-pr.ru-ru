---
description: Атрибут Color задает цвет пера.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Цвет пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544426"
---
# <a name="pen-color"></a>Цвет пера

Атрибут Color задает цвет пера. Приложение может создать косметический перо с уникальным цветом с помощью макроса [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) для хранения красного, зеленого, синего Triplet, указывающего нужный цвет в структуре [COLORREF](colorref.md) , и передачи адреса этой структуры в функцию [**креатепен**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**креатепениндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)или [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . (Стандартные перья ограничены черным, белым и невидимыми.) Дополнительные сведения о триады и цветах RGB см. в разделе [цвета](colors.md).

 

 



