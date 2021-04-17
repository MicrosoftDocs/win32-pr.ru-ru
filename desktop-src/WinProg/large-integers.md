---
title: Большие целые числа
description: Большие целочисленные функции и структуры изначально поддерживали 64-разрядные значения в 32-разрядной версии Windows.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- большие целые числа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700921"
---
# <a name="large-integers"></a>Большие целые числа

Большие целочисленные функции и структуры изначально поддерживали 64-разрядные значения в 32-разрядной версии Windows. Теперь компилятор C может поддерживать 64-разрядные целые числа в собственном коде. Например, Microsoft Visual C++ поддерживает целочисленный тип с размером [**\_ \_ Int64**](/windows/desktop/Midl/--int64) . Дополнительные сведения см. в документации, входящей в состав компилятора C.

Сведения о 64-разрядных целых числах в 64-разрядной версии Windows см. [в разделе новые типы данных](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Операции с большими целочисленными значениями

Приложения могут умножить 32-разрядные целые числа со знаком или без знака, создавая 64-разрядные результаты с помощью функций [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) и [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) . Приложения могут сдвинуть биты в 64-битных значениях влево или вправо с помощью функций [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)и [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) . Эти функции обеспечивают логическую и арифметическую смену.

Приложения также могут умножить и разделить 32-битные значения в одной операции с помощью функции [**мулдив**](/windows/desktop/api/Winbase/nf-winbase-muldiv) . Хотя результатом операции является 32-разрядное значение, функция сохраняет промежуточный результат в виде 64-разрядного значения, чтобы информация не была потеряна при умножении и разделении больших 32-разрядных значений.

## <a name="large-integer-reference"></a>Ссылка на большое целое число

-   [Большие целочисленные функции](large-integer-functions.md)
-   [Структуры больших целых чисел](large-integer-structures.md)

 

 