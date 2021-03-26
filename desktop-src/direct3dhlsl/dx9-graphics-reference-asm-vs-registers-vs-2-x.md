---
title: Регистры — vs_2_x
description: В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 2 \_ x.
ms.assetid: 35dfa3c8-be8e-4b2b-84c4-766850cf146c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6aebd9095e18abd5ac76988e46c2e061e30209c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777939"
---
# <a name="registers---vs_2_x"></a>Регистры — VS \_ 2 \_ x

В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 2 \_ x.

## <a name="input-registers"></a>Входные регистры



| Регистрация | Имя                                                                                      | Count      | Чтение-запись | \# Чтение портов | \# Операций чтения и inst | Измерение | реладдр | Значения по умолчанию     | Требуется ДКЛ |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| 3,3\#      | [Входной регистр](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Неограниченно       | 4         | нет      | См. Примечание 1   | Да          |
| Cерверный\#      | [Временный регистр](dx9-graphics-reference-asm-vs-registers-temporary.md)               | См. примечание 2 | Чтение-запись | 3             | Неограниченно       | 4         | нет      | None         | Нет           |
| c\#      | [Регистр постоянного float](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | См. Примечание 3 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | Нет           |
| a0       | [Регистр адресов](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | Чтение-запись | 1             | 2               | 4         | нет      | None         | Нет           |
| &\#      | [Постоянный логический регистр](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Нет      | FALSE        | Нет           |
| сохранении\#      | [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | нет      | (0, 0, 0, 0) | Нет           |
| aL       | [Регистр счетчика цикла](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Нет      | None         | Нет           |
| P0       | [Регистр предиката](dx9-graphics-reference-asm-vs-registers-predicate.md)               | 1          | Чтение-запись | 1             | 1               | 4         | нет      | None         | Нет           |



 

Примечания.

1.  Partial (0, 0, 0, 1) — Если обновляется только подмножество каналов, остальные каналы будут по умолчанию иметь значение (0, 0, 0, 1).
2.  Равно D3DCAPS9. VS20Caps. Нумтемпс (не менее 12 для VS \_ 2 \_ x).
3.  Равно D3DCAPS9. Максвертексшадерконст (по крайней мере 256 для VS \_ 2 \_ x).

## <a name="output-registers"></a>Выходные регистры



| Регистрация | Имя                                                                                          | Count | Чтение-запись | Измерение | реладдр | Значения по умолчанию | Требуется ДКЛ |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Регистр позиций](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | нет      | None     | Нет           |
| офог     | [Регистр тумана](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Нет      | None     | Нет           |
| Решает     | [Регистр размера точки](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Нет      | None     | Нет           |
| oD\#     | [Регистр цвета](dx9-graphics-reference-asm-vs-registers-color.md); См. Примечание 1               | 2     | W   | 4         | нет      | None     | Нет           |
| Наблюдения\#     | [Регистр координаты текстуры](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | нет      | None     | Нет           |



 

Примечания.

-   oD0 — это вывод рассеянного цвета; oD1 — это вывод отраженного цвета.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




