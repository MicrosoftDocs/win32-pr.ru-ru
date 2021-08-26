---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Эти плоские функции API упаковываются с помощью класса Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Функции кисти (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afdec5667dfcfe4b83e54af3fc0b88fcef991494e36f1e4788062029d1d6e29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888344"
---
# <a name="brush-functions-gdi"></a>Функции кисти (GDI+)

Windows GDI+ предоставляет плоский API, который состоит из примерно 600 функций, реализованных в Gdiplus.dll и объявленных в гдиплусфлат. h. функции в GDI+ плоском API упаковываются в коллекцию из примерно 40 классов C++. Не рекомендуется напрямую вызывать функции в плоском API. всякий раз, когда вы вызываете GDI+, это необходимо сделать, вызвав методы и функции, предоставляемые оболочками C++. Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API. дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ плоский API](-gdiplus-flatapi-flat.md).

Следующие плоские функции API упаковываются с помощью класса [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Функции-кисти и соответствующие методы-оболочки



| Плоская функция                                                                        | Метод-оболочка                                          | Описание                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Гпстатус ВИНГДИПАПИ Гдипклонебруш ( \* кисть гпбруш, гпбруш \* \* клонебруш)          | [**Кисть:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | Метод [**Brush:: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) создает новый объект [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) на основе этой кисти. |
| Гпстатус ВИНГДИПАПИ Гдипделетебруш ( \* кисть гпбруш)                                 | Виртуальная ~ Brush ()                                        | Очищает ресурсы, используемые объектом [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .                                                                    |
| Гпстатус ВИНГДИПАПИ Гдипжетбруштипе ( \* кисть гпбруш, \* тип гпбруштипе)<br/> | [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | Метод [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) получает тип этой кисти.                                                      |



 

 

 




