---
description: Используйте эту заметку для определения содержимого внешнего файла в качестве значения инициализации для параметра effect.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Аннотация инициализации параметра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262319"
---
# <a name="parameter-initialization-annotation"></a>Аннотация инициализации параметра

Используйте эту заметку для определения содержимого внешнего файла в качестве значения инициализации для параметра effect. Пример:


```
string SasResourceAddress = "Value";
```



где value — это текстовая строка ASCII, которая может содержать абсолютный или относительный путь. Относительный путь относится к каталогу, содержащему файл эффектов.

Пример:


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



Значение по умолчанию - пустая строка.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по стандарту DirectX для заметок и семантик](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



