---
description: ICEM07 проверяет, что порядок файлов в таблице последовательности соответствует порядку файлов в MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910384"
---
# <a name="icem07"></a>ICEM07

ICEM07 проверяет, что порядок файлов в таблице последовательности соответствует порядку файлов в [MergeModule.CABinet](mergemodule-cabinet.md).

Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.

## <a name="result"></a>Результат

ICEM07 отправляет сообщение об ошибке, если порядок файлов в таблице файлов не соответствует порядку в CAB-файле.

## <a name="example"></a>Пример

IC0M07 выводит следующее сообщение об ошибке для приведенного примера.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[Таблица файлов](file-table.md)



| Файл          | Последовательность |
|---------------|----------|
| Файл а. *GUID1* | 1        |
| Филеб. *GUID1* | 8        |
| Филек. *GUID1* | 52       |



 

Внедренный [MergeModule.CABinet](mergemodule-cabinet.md)



| Файл          |
|---------------|
| Файл а. *GUID1* |
| Филек. *GUID1* |
| Подан. *GUID1* |
| Филеб. *GUID1* |



 

Хотя порядковые номера файлов в таблице файлов не должны быть последовательными, а в CAB-файле могут содержаться дополнительные файлы, относительная последовательность всех файлов в таблице File должна соответствовать порядку в [MergeModule.CABinet](mergemodule-cabinet.md). Чтобы устранить эту ошибку, измените порядковый номер Филеб на Филек, чтобы он совпадал с порядком файлов в CAB-файле, или перестройте CAB-файл с файлами в правильном порядке.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ссылка на модуль слияния ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



