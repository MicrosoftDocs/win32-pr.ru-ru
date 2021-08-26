---
title: Регистры — vs_2_0
description: В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 2 \_ 0.
ms.assetid: e5ef015e-1e4d-41b3-95da-3b44ef0bd73e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd31f4ce5cac538624fe736642b30cbee9ba54579ee50da9a2ccd027847e9ecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067974"
---
# <a name="registers---vs_2_0"></a>Регистры — VS \_ 2 \_ 0

В этом разделе содержатся справочные сведения по входным и выходным регистрам, реализованным построителем вершин версии 2 \_ 0.

## <a name="input-registers"></a>Входные регистры



| Зарегистрировать | Имя                                                                                      | Count      | Чтение-запись | \# Чтение портов | \# Операций чтения и inst | Измерение | реладдр | Умолчания;     | Требуется ДКЛ |
|----------|-------------------------------------------------------------------------------------------|------------|-----|---------------|-----------------|-----------|---------|--------------|--------------|
| 3,3\#      | [Входной регистр](dx9-graphics-reference-asm-vs-registers-input.md)                       | 16         | R   | 1             | Без ограничений       | 4         | нет      | См. примечание 1   | Да          |
| Cерверный\#      | [Временный регистр](dx9-graphics-reference-asm-vs-registers-temporary.md)               | 12         | Чтение-запись | 3             | Без ограничений       | 4         | нет      | Нет         | Нет           |
| c\#      | [Регистр постоянного float](dx9-graphics-reference-asm-vs-registers-constant-float.md)     | См. примечание 2 | R   | 1             | 2               | 4         | a0/aL | (0, 0, 0, 0) | Нет           |
| a0       | [Регистр адресов](dx9-graphics-reference-asm-vs-registers-address.md)                   | 1          | Чтение-запись | 1             | 2               | 4         | нет      | Нет         | Нет           |
| b\#      | [Постоянный логический регистр](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) | 16         | R   | 1             | 1               | 1         | Нет      | FALSE        | Нет           |
| сохранении\#      | [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md) | 16         | R   | 1             | 1               | 4         | нет      | (0, 0, 0, 0) | Нет           |
| aL       | [Регистр счетчика цикла](dx9-graphics-reference-asm-vs-registers-loop-counter.md)         | 1          | R   | 1             | 2               | 1         | Нет      | Нет         | Нет           |



 

Примечания.

1.  Partial (0, 0, 0, 1) — Если обновляется только подмножество каналов, остальные каналы будут по умолчанию иметь значение (0, 0, 0, 1).
2.  Равно D3DCAPS9. Максвертексшадерконст (по крайней мере 256 для VS \_ 2 \_ 0).

## <a name="output-registers"></a>Выходные регистры



| Зарегистрировать | Имя                                                                                          | Count | Чтение-запись | Измерение | реладдр | Умолчания; | Требуется ДКЛ |
|----------|-----------------------------------------------------------------------------------------------|-------|-----|-----------|---------|----------|--------------|
| oPos     | [Регистр позиций](dx9-graphics-reference-asm-vs-registers-position.md)                     | 1     | W   | 4         | нет      | Нет     | Нет           |
| офог     | [Регистр тумана](dx9-graphics-reference-asm-vs-registers-fog.md)                               | 1     | W   | 1         | Нет      | Нет     | Нет           |
| Решает     | [Регистр размера точки](dx9-graphics-reference-asm-vs-registers-point-size.md)                 | 1     | W   | 1         | Нет      | Нет     | Нет           |
| oD\#     | [Регистр цвета](dx9-graphics-reference-asm-vs-registers-color.md); См. Примечание 1               | 2     | W   | 4         | нет      | Нет     | Нет           |
| Наблюдения\#     | [Регистр координаты текстуры](dx9-graphics-reference-asm-vs-registers-texture-coordinate.md) | 8     | W   | 4         | нет      | Нет     | Нет           |



 

Примечания.

-   oD0 — это вывод рассеянного цвета; oD1 — это вывод отраженного цвета.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




