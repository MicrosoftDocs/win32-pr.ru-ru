---
title: Удаление атрибутов метаданных
description: Удаление атрибутов метаданных
ms.assetid: 44546091-406f-4ae6-914a-942d1b89e0e4
keywords:
- Windows Media Format SDK, удаление атрибутов метаданных
- Расширенный системный формат (ASF), удаление атрибутов метаданных
- ASF (Расширенный системный формат), удаление атрибутов метаданных
- метаданные, удаление атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b10176452dcc78cc3eca898b61c350a157e568
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "104412693"
---
# <a name="removing-metadata-attributes"></a>Удаление атрибутов метаданных

Атрибут метаданных можно удалить, передав его индекс и номер потока в метод [**IWMHeaderInfo3::D елетеаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-deleteattribute) . Порядок, в котором оставшиеся атрибуты индексируются после удаления атрибута, не изменяется. все оставшиеся атрибуты, для которых изначально было задано значение индекса больше, чем у удаляемого значения индекса, уменьшаются на один. При удалении нескольких атрибутов сделайте это в порядке убывания по индексу, чтобы не вычислять коррекцию при индексировании.

Для удобства удаления значений метод [**IWMHeaderInfo3:: жетаттрибутеиндицес**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) возвращает значения индекса в порядке убывания.

> [!Note]  
> Значения индекса, полученные с помощью методов [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) , несовместимы со значениями индекса, полученными с помощью методов [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo). При использовании методов одного интерфейса для изменения атрибутов в файле следует предположить, что все значения индекса, ранее извлеченные из другого интерфейса, больше не являются допустимыми и должны быть получены снова. По возможности следует избегать использования методов **ивмхеадеринфо** .

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Работа с метаданными**](working-with-metadata.md)
</dt> </dl>

 

 




