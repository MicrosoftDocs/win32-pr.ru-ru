---
description: С помощью функций Енумфонтс и EnumFontFamilies можно перечислить шрифты, доступные в контексте устройства памяти, совместимого с принтерами.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Проверка возможностей текста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997418"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Проверка возможностей текста устройства

С помощью функций [енумфонтс](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) и [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) можно перечислить шрифты, доступные в контексте устройства памяти, совместимого с принтерами. Можно также использовать функцию [жетдевицекапс](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) для получения сведений о возможностях текста устройства. Вызывая функцию [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) с индексом нумфонтс, можно определить минимальное число шрифтов, поддерживаемых принтером. (Отдельный принтер может поддерживать больше шрифтов, чем указано в возвращаемом значении из **жетдевицекапс** с индексом нумфонтс.) С помощью индекса ТЕКСТКАПС можно вычислить многие текстовые возможности указанного устройства.

 

 
