---
description: ICE71 проверяет, содержит ли таблица мультимедиа запись с DiskId, равным 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999242"
---
# <a name="ice71"></a>ICE71

ICE71 проверяет, содержит ли [Таблица мультимедиа](media-table.md) запись с DiskId, равным 1. (Установщик Windows предполагает, что пакет MSI находится на диске 1.)

## <a name="result"></a>Результат

ICE71 возвращает ошибку, если таблица мультимедиа не содержит запись с DiskId, равным 1.

## <a name="example"></a>Пример

ICE71 сообщает об ошибке в приведенном примере.

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

T0 исправить эту ошибку, измените DiskId записи, в которой хранится пакет, равным 1.

[Таблица мультимедиа](media-table.md) (частичная)



| DiskId |
|--------|
| 2      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



