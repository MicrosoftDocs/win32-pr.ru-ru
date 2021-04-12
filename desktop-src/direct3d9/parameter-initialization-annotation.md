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
# <a name="parameter-initialization-annotation"></a><span data-ttu-id="ce613-103">Аннотация инициализации параметра</span><span class="sxs-lookup"><span data-stu-id="ce613-103">Parameter Initialization Annotation</span></span>

<span data-ttu-id="ce613-104">Используйте эту заметку для определения содержимого внешнего файла в качестве значения инициализации для параметра effect.</span><span class="sxs-lookup"><span data-stu-id="ce613-104">Use this annotation to define the contents of an external file as the initialization value for an effect parameter.</span></span> <span data-ttu-id="ce613-105">Пример:</span><span class="sxs-lookup"><span data-stu-id="ce613-105">For example:</span></span>


```
string SasResourceAddress = "Value";
```



<span data-ttu-id="ce613-106">где value — это текстовая строка ASCII, которая может содержать абсолютный или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="ce613-106">where Value is an ASCII text string that may contain an absolute or relative path.</span></span> <span data-ttu-id="ce613-107">Относительный путь относится к каталогу, содержащему файл эффектов.</span><span class="sxs-lookup"><span data-stu-id="ce613-107">A relative path is relative to the directory that contains the effect file.</span></span>

<span data-ttu-id="ce613-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="ce613-108">Here is an example:</span></span>


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



<span data-ttu-id="ce613-109">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="ce613-109">The default value is an empty string.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce613-110">См. также</span><span class="sxs-lookup"><span data-stu-id="ce613-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce613-111">Справочник по стандарту DirectX для заметок и семантик</span><span class="sxs-lookup"><span data-stu-id="ce613-111">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



