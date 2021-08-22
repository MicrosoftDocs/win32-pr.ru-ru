---
description: Синхронизированный доступный мультимедийный обмен (SAMI) — это формат для добавления субтитров к цифровым носителям.
ms.assetid: 007c8181-089e-4e56-a31d-9d1942f90b07
title: Источник носителя SAMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7567f7479b6f8d0d2439f89dbf3e6cf273fc7dcae31590ddf9b51a4d66a6940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034822"
---
# <a name="sami-media-source"></a>Источник носителя SAMI

Синхронизированный доступный мультимедийный обмен (SAMI) — это формат для добавления субтитров к цифровым носителям. Заголовки хранятся в отдельном текстовом файле с расширением. SMI или. Sami.

В Media Foundation файлы заголовков SAMId поддерживаются через источник носителя SAMI. Используйте [сопоставитель источников](source-resolver.md) , чтобы создать экземпляр источника носителя Sami из URL-адреса или потока байтов. Media Foundation не предоставляет компонент, который отображает субтитры SAMId. Приложение должно интерпретировать данные заголовка, полученные от источника на носителе SAMI.

Ниже приведен пример файла SAMI.

``` syntax
<SAMI>
<HEAD>
    <STYLE TYPE="text/css">
    <!--
    P {
        font-family: Arial;
        background: #000000;
        text-align: center;
        }

#standard {Name: Standard; color: #FFFFFF; font-size: 14pt; } 
#hilite {Name: Youth; color: greenyellow; font-size: 18pt;}

    .ENUSCC { Name: English; lang: EN-US-CC; }
    .FRFRCC { Name: French; lang: fr-FR; } 

    -->
    </STYLE>
</HEAD>
<BODY>
    <SYNC Start="0">
        <P Class="ENUSCC">The <I>first</I> caption.</P>
        <P Class="FRFRCC">Un</P>
    </SYNC>
    <SYNC Start="3000">
        <P Class="ENUSCC">The <I>second</I> caption.</P>
        <P Class="FRFRCC">Deux</P>
    </SYNC>
    <SYNC Start="5000">
        <P Class="ENUSCC">The <I>third</I> caption.</P>
        <P Class="FRFRCC">Trois</P>
    </SYNC>
</BODY>
</SAMI>
```

`<STYLE>`Элемент содержит сведения о стиле. Этот пример содержит базовый стиль для `<P>` элементов, а также два именованных стиля: "Стандартный" и "хилите". Именованные стили используются для изменения базового стиля. Заголовки помещаются в `<SYNC>` элементы. Атрибут start задает время презентации в миллисекундах для этого заголовка. Заголовки в этом примере приведены на двух языках, указанных в тегах языка RFC-1766, «EN-US» и «fr-FR». В заголовках языки идентифицируются по именам их классов. в этом случае "ЕНУСКК" и "ФРФРКК".

Источник носителя SAMId создает один поток мультимедиа для каждого языка. По умолчанию выбирается первый поток, и оставшиеся выбранные потоки отменяются. Приложение может изменить выбор потока, вызвав [**имфпресентатиондескриптор:: селектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) и [**Имфпресентатиондескриптор::D еселектстреам**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream). Каждый дескриптор потока содержит следующие атрибуты.



| attribute                                                       | Описание                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| [**\_язык MF SD \_**](mf-sd-language-attribute.md)            | Тег языка, заданный `lang` атрибутом.  |
| [**\_язык MF SD \_ Sami \_**](mf-sd-sami-language-attribute.md) | Имя языка, заданное `Name` атрибутом. |



 

Каждый поток имеет следующий тип носителя:



| attribute                                                                            | Значение                 |
|--------------------------------------------------------------------------------------|-----------------------|
| [**\_ \_ основной тип MF \_ MT**](mf-mt-major-type-attribute.md)                            | **Мфмедиатипе \_ Sami** |
| [**MF \_ — \_ все \_ \_ независимые примеры**](mf-mt-all-samples-independent-attribute.md) | **TRUE**              |



 

Источник SAMI предоставляет каждый заголовок в отдельном образце носителя. Образец метки времени и длительность являются производными от `<SYNC>` элемента. Буфер мультимедиа, содержащийся в примере, содержит заголовок в виде текста ASCII. Стиль заголовка внедряется в заголовок в виде встроенного `STYLE` атрибута. Например, при наличии предыдущего файла SAMI и использовании в потоке английского языка со стилями по умолчанию первый буфер мультимедиа будет содержать следующие данные. (Разрывы строк могут отличаться от показанных здесь.)

``` syntax
<P STYLE="
    font-family: Arial;
    background: #000000;
    text-align: center;
    Name: English; lang: EN-US-CC;  
    Name: Standard; color: #FFFFFF; 
    font-size: 14pt; ">The<I>first</I> caption.
```

## <a name="sami-styles"></a>Стили SAMI

Чтобы изменить текущий стиль, используйте интерфейс [**имфсамистиле**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) . Этот интерфейс получается путем вызова [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в источнике носителя Sami. (Если вы используете источник мультимедиа SAMI с сеансом мультимедиа, вызовите метод **WebService** в сеансе мультимедиа.) Идентификатор службы — это **\_ \_ Служба MF Sami**.

В следующем примере задается текущий стиль SAMI, заданный параметром index.


```C++
HRESULT SetSAMIStyleByIndex(IMFMediaSource *pSource, DWORD index)
{
    IMFSAMIStyle *pSami = NULL;

    DWORD cStyles;
    PROPVARIANT varStyles;

    HRESULT hr = MFGetService(pSource, MF_SAMI_SERVICE, IID_PPV_ARGS(&pSami));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->GetStyleCount(&cStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    if (index >= cStyles)
    {
        hr = E_INVALIDARG;
        goto done;
    }

    hr = pSami->GetStyles(&varStyles);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSami->SetSelectedStyle(varStyles.calpwstr.pElems[index]);

done:
    PropVariantClear(&varStyles);
    SafeRelease(&pSami);
    return hr;
}
```



Этот пример вызывает следующие методы в источнике носителя SAMI:

-   [**Имфсамистиле:: жетстилекаунт**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstylecount) возвращает число стилей.
-   [**Имфсамистиле::**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-getstyles) возвращает список имен стилей, сохраненных в **пропвариант**.
-   [**Имфсамистиле:: сетселектедстиле**](/windows/desktop/api/mfidl/nf-mfidl-imfsamistyle-setselectedstyle) задает стиль по имени.

Список имен стилей также хранится в дескрипторе презентации в атрибуте [**MF \_ PD \_ Sami \_ стилелист**](mf-pd-sami-stylelist-attribute.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Источники и приемники мультимедиа](media-sources-and-sinks.md)
</dt> <dt>

[Поддерживаемые форматы мультимедиа в Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



