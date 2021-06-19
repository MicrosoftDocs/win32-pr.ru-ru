---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Эти плоские функции API упаковываются с помощью класса Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Функции Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395089"
---
# <a name="brush-functions-gdi"></a>Функции Brush (GDI+)

Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций, которые реализуются в Gdiplus.dll и объявлены в Гдиплусфлат. h. Функции в плоском API-интерфейсе GDI+ упаковываются в коллекцию из примерно 40 классов C++. Не рекомендуется напрямую вызывать функции в плоском API. При каждом вызове GDI+ это следует делать путем вызова методов и функций, предоставляемых оболочками C++. Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API. Дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Следующие плоские функции API упаковываются с помощью класса [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Функции-кисти и соответствующие методы-оболочки



| Плоская функция                                                                        | Метод-оболочка                                          | Описание                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Гпстатус ВИНГДИПАПИ Гдипклонебруш ( \* кисть гпбруш, гпбруш \* \* клонебруш)          | [**Кисть:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | Метод [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) создает новый объект [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) на основе этой кисти. |
| Гпстатус ВИНГДИПАПИ Гдипделетебруш ( \* кисть гпбруш)                                 | Виртуальная ~ Brush ()                                        | Очищает ресурсы, используемые объектом [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .                                                                    |
| Гпстатус ВИНГДИПАПИ Гдипжетбруштипе ( \* кисть гпбруш, \* тип гпбруштипе)<br/> | [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | Метод [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) получает тип этой кисти.                                                      |



 

 

 




