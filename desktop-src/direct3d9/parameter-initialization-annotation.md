---
description: Используйте эту заметку для определения содержимого внешнего файла в качестве значения инициализации для параметра effect.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Аннотация инициализации параметра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798669"
---
# <a name="parameter-initialization-annotation"></a>Аннотация инициализации параметра

Используйте эту заметку для определения содержимого внешнего файла в качестве значения инициализации для параметра effect. Например:


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



Значение по умолчанию — пустая строка.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по стандарту DirectX для заметок и семантик](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



