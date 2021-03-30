---
description: Объявление сведений о фильтре
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Объявление сведений о фильтре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806707"
---
# <a name="declaring-filter-information"></a>Объявление сведений о фильтре

Первый шаг — объявить сведения о фильтре, если это необходимо. DirectShow определяет следующие структуры для описания фильтров, ПИН-кодов и типов мультимедиа:



| Структура                                               | Описание             |
|---------------------------------------------------------|-------------------------|
| [**\_Фильтр амовиесетуп**](amoviesetup-filter.md)       | Описывает фильтр.     |
| [**\_ПИН-код амовиесетуп**](amoviesetup-pin.md)             | Описывает ПИН-код.        |
| [**АМОВИЕСЕТУП \_ MEDIATYPE**](amoviesetup-mediatype.md) | Описывает тип мультимедиа. |



 

Эти структуры являются вложенными. Структура **\_ фильтра амовеиесетуп** имеет указатель на массив амовиесетупных координатных структур, и каждый из них имеет указатель на массив из **амовеиесетупных структур \_ MEDIATYPE** . **\_** Вместе эти структуры предоставляют достаточно информации для того, чтобы интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) обнаружил фильтр. Они не являются полным описанием фильтра. Например, если фильтр создает несколько экземпляров одного и того же ПИН-кода, следует объявить для него только одну [**амовиесетупую структуру \_ ПИН**](amoviesetup-pin.md) -кода. Кроме того, фильтр не требуется для поддержки каждого сочетания типов файлов мультимедиа, которые он регистрирует. Кроме того, не требуется регистрировать каждый поддерживаемый тип мультимедиа.

Объявите структуры Set-up в виде глобальных переменных в библиотеке DLL. В следующем примере показан фильтр с одним выходным закреплением:


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



Имя фильтра объявляется как статическая глобальная переменная, так как она будет использоваться в других местах.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Как зарегистрировать фильтры DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



