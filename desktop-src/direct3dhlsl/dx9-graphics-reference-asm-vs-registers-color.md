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
ms.openlocfilehash: b19850985002ad9c36a6a6366f744106cb041db858f9df9b755996e114fdf6c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512290"
---
# <a name="color-register"></a>Регистр цвета

Эти регистры выходных данных шейдера вершин содержат значение цвета. 

| Зарегистрировать | Описание              |
|----------|--------------------------|
| oD0      | Регистр цветов диффузии.  |
| oD1      | Регистр отраженного цвета. |



 

Значение oD0 интерполяции и записывается в цветовую область шейдера пикселей 0 (v0). Значение oD1 интерполяции и записывается в цветовой реестр построителя текстуры 1 (v1). Дополнительные сведения о цветовых регистрах шейдера пикселей см. в разделе [регистр цветов ввода](dx9-graphics-reference-asm-ps-registers-input-color.md) построителя текстуры.

## <a name="remarks"></a>Remarks

Пример


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




