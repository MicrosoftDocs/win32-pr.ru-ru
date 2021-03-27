---
title: Регистр цвета
description: Эти регистры выходных данных шейдера вершин содержат значение цвета.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350872"
---
# <a name="color-register"></a>Регистр цвета

Эти регистры выходных данных шейдера вершин содержат значение цвета. 

| Регистрация | Описание              |
|----------|--------------------------|
| oD0      | Регистр цветов диффузии.  |
| oD1      | Регистр отраженного цвета. |



 

Значение oD0 интерполяции и записывается в цветовую область шейдера пикселей 0 (v0). Значение oD1 интерполяции и записывается в цветовой реестр построителя текстуры 1 (v1). Дополнительные сведения о цветовых регистрах шейдера пикселей см. в разделе [регистр цветов ввода](dx9-graphics-reference-asm-ps-registers-input-color.md) построителя текстуры.

## <a name="remarks"></a>Remarks

Пример


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




