---
title: Сохранение 64-разрядного значения
description: Чтобы сохранить 64-разрядное значение указателя, используйте ULONG \_ ptr. При компиляции с помощью компилятора с \_ 64-разрядным компилятором значение типа ULONG 32 бит при компиляции с 32-разрядным компилятором и 64 бит.
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- хранение 64-разрядных значений 64-bit Windows программирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469071"
---
# <a name="storing-a-64-bit-value"></a>Сохранение 64-разрядного значения

Чтобы сохранить 64-разрядное значение указателя, используйте **ulong \_ ptr**. При компиляции с помощью компилятора с 64-разрядным компилятором значение **\_ типа ulong** 32 бит при компиляции с 32-разрядным компилятором и 64 бит.

В следующих примерах используется реальный код, перенесенный в 64-разрядный Windows. Комментирование действий по добавлению кода, совместимого с 64-разрядной версией.

## <a name="example-1-getting-an-address"></a>Пример 1. получение адреса

Следующий код иллюстрирует переносимый способ получения адреса.




| | | Использование ULONG (только 32-разрядный метод) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | | Использование ULONG_PTR (переносимый метод) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>Пример 2. Вычисление адреса

Следующий код иллюстрирует переносимый способ вычисления адреса.




| | | Использование ULONG (только 32-разрядный метод) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | | Использование ULONG_PTR (переносимый метод) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




