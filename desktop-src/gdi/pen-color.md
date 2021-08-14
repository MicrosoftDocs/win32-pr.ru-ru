---
description: Атрибут Color задает цвет пера.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Цвет пера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886209"
---
# <a name="pen-color"></a>Цвет пера

Атрибут Color задает цвет пера. Приложение может создать косметический перо с уникальным цветом с помощью макроса [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) для хранения красного, зеленого, синего Triplet, указывающего нужный цвет в структуре [COLORREF](colorref.md) , и передачи адреса этой структуры в функцию [**креатепен**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**креатепениндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)или [**ексткреатепен**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . (Стандартные перья ограничены черным, белым и невидимыми.) Дополнительные сведения о триады и цветах RGB см. в разделе [цвета](colors.md).

 

 



