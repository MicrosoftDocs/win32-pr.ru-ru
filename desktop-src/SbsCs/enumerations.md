---
description: Сведения о перечислениях, используемых в параллельных API-интерфейсах сборок, таких как ASM_CMP_FLAGS и CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Параллельные перечисления сборок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a7aee5c64209176ce0690c0a9e7954ad51160a0723c1ec5d1e7e4cee5dba1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142217"
---
# <a name="side-by-side-assembly-enumerations"></a>Параллельные перечисления сборок

Параллельный API сборки использует следующие перечисления.



| Перечисление                                                         | Описание                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Флаги ASM CMP**](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | Используется методом [**Equals**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) для указания, какие части двух имен сборок следует сравнить.                                                                       |
| [**\_ \_ Флаги вывода ASM**](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | Используется [**методом,**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) чтобы указать, какие части имени параллельной сборки следует включить в строковое представление имени. |
| [**\_имя ASM**](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | Идентификаторы свойств для пар "имя-значение" в имени параллельной сборки.                                                                                                                    |
| [**СОЗДАТЬ \_ \_ имя ASM \_ \_ Флаги obj**](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | Используется функцией [**креатеассемблинамеобжект**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) для указания параллельного имени сборки.                                                               |



 

 

 



