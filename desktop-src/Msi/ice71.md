---
description: ICE71 проверяет, содержит ли таблица мультимедиа запись с DiskId, равным 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1090eb8b1a36ed361ef763bfda3875a8fde052ed8643dceeb660c88ae954a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142518"
---
# <a name="ice71"></a>ICE71

ICE71 проверяет, содержит ли [Таблица мультимедиа](media-table.md) запись с DiskId, равным 1. (установщик Windows предполагает, что пакет .msi находится на диске 1.)

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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



