---
description: В примере кистей используются регионы для имитации &\# 0034; с масштабированием&\# 0034; представление растрового изображения размером 8 в 8 пикселей.
ms.assetid: a8e0cbfe-f05b-46ae-b420-ae34a5efbff3
title: Использование регионов для проверки попадания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d553eeaf37b954d0ec9d0b8897df98cf1a513d7ca7212ca82bc376afe1fc7163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558124"
---
# <a name="using-regions-to-perform-hit-testing"></a>Использование регионов для проверки попадания

В примере в [кистях](brushes.md) используются регионы для имитации "масштабированного" изображения с монохромным изображением размером 8 пикселей. Щелкая Пиксели в этом битовом рисунке, пользователь создает пользовательскую кисть, подходящую для операций рисования. В примере показано, как использовать функцию [**птинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) для проверки попадания и функции [**инвертргн**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn) для инвертирования цветов в области.

 

 



