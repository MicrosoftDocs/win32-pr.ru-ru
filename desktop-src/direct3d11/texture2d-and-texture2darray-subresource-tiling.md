---
title: Размещение на плитках вложенных ресурсов Texture2D и Texture2DArray
description: В таблицах ниже показано, как размещаются на плитках вложенные ресурсы Texture2D и Texture2DArray.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7cc181845785ab978dc5d58b1e131a7f32c34a6d04006af1ac8034f089ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530439"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Размещение на плитках вложенных ресурсов Texture2D и Texture2DArray

В этих таблицах показано, как [**подTexture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и перемещаются подресурсы [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) . Значения в этих таблицах не учитывают упаковку хвостовых MIP-карт.

В этой таблице показано, как размещаются на плитках вложенные ресурсы [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) с множественной дискретизацией и одной выборкой.



| Бит/пкс (1 семпл/пкс) | Размеры плиток (пиксели, ШxВ) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | 256x128                       |
| 32                          | 128x128                       |
| 64                          | 128x64                        |
| 128                         | 64x64                         |
| BC1,4                       | 512x256                       |
| BC2,3,5,6,7                 | 256x256                       |



 

Число битов формата не поддерживается для мозаичных ресурсов: 96, форматы видео, формат DXGI \_ \_ R1 \_ UNORM, формат DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM и DXGI \_ Format \_ R8R8 G8B8 UNORM \_ \_ .

В этой таблице показано, как размещаются на плитках вложенные ресурсы [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) и [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) с множественной дискретизацией и различным числом выборок.



| Число выборок           | Разделить размеры мозаики выше на (Вксх) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Для использования с мозаичным ресурсом необходимо использовать только счетчики выборки 1 и 4. В настоящее время мозаичные ресурсы не поддерживают 2, 8 и 16, даже если они показаны.

Реализации могут поддерживать 2, 8 и/или 16 образцов многовыборочного сглаживания (MSAA) для ресурсов без мозаичного заполнения, даже если они не поддерживаются мозаичным ресурсом.

Мозаичные ресурсы с количеством выборок больше 1 не могут использовать форматы в 128 бит/с.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Мозаичное заполнение области мозаичного ресурса](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 