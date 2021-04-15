---
description: Работа с текстовыми строками DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Работа с текстовыми строками DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662668"
---
# <a name="working-with-dvd-text-strings"></a>Работа с текстовыми строками DVD

Некоторые диски DVD, особенно диски Караоке, могут содержать список текстовых строк, которые дополняют видео-или аудио-содержимое. Эти текстовые строки содержат метаданные о содержимом, такие как названия песен, имена исполнителей, сведения о жанрах и т. д. Текстовые строки могут присутствовать на нескольких языках. Эти строки являются необязательными, и многие диски их не используют.

Чтобы получить текстовые строки с DVD-диска, используйте интерфейс [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , предоставляемый [навигатором DVD](dvd-navigator-filter.md). Для получения текстовых строк не нужно создавать граф воспроизведения DVD-дисков. Можно просто создать DVD-навигатор, задать громкость DVD, а затем вызвать соответствующие методы строки текста:



| Метод                                                                                  | Описание                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2:: Жетдвдтекстнумберофлангуажес**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | Возвращает число языков, для которых имеются текстовые строки.                                                                                                                                  |
| [**IDvdInfo2:: Жетдвдтекстлангуажеинфо**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | Возвращает сведения о текстовых строках для одного языка.                                                                                                                                       |
| [**IDvdInfo2:: Жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | Возвращает текстовую строку для указанного языка по индексу.                                                                                                                                          |
| [**IDvdInfo2:: Жетдвдтекстстрингаснативе**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | Возвращает текстовую строку в виде массива необработанных байтов. Используйте этот метод, если текстовая строка использует кодировку символов, не поддерживаемую [**жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode). |



 

Ниже приведена базовая процедура получения текстовых строк.

1.  Вызовите метод [**IDvdInfo2:: жетдвдтекстнумберофлангуажес**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) , чтобы найти общее число языков, в которых отображаются текстовые строки. Если это число равно нулю, значит, DVD-диск не содержит текстовых строк. (Это, вероятно, наиболее распространенный случай.)
2.  Если число языков не меньше одного, вызовите [**IDvdInfo2:: жетдвдтекстлангуажеинфо**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) , чтобы получить сведения о каждом языке. Язык указывается с помощью индекса. Метод возвращает общее количество текстовых строк на этом языке, код локали (**LCID**) для языка и кодировку символов (Unicode или другой). Текстовые строки DVD могут использовать несколько различных наборов символов. они перечислены в [**\_ перечислении текстчарсет DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).
3.  Чтобы получить текстовую строку, вызовите метод [**IDvdInfo2:: жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) или [**IDvdInfo2:: жетдвдтекстстрингаснативе**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative). Первый метод возвращает строку расширенных символов, но не поддерживает каждый набор символов. Второй метод возвращает массив байтов, содержащий необработанные текстовые данные. Для обоих методов можно вызвать метод с указателем буфера **null** , чтобы определить размер строки и тип текста. Затем выделите буфер и снова вызовите метод, чтобы получить строку.

Каждая текстовая строка имеет связанный код идентификатора, который указывает значение текстовой строки. Идентификатор возвращается в виде значения [**\_ текстстрингтипе DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) . Существует две категории идентификатора: *идентификаторы структуры* и *идентификаторы содержимого*. Идентификаторы структуры имеют числовые коды в диапазоне 0x00 – 0x02F. Идентификаторы содержимого имеют диапазон 0x30 и выше. (Перечисление **\_ текстстрингтипе DVD** определяет подмножество наиболее распространенных идентификаторов, но методы [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) могут возвращать код идентификатора.) Идентификатор структуры описывает логическую часть DVD-диска, например том, заголовок или часть названия (PTT). Идентификатор содержимого указывает значение конкретной текстовой строки, например название фильма, название песни или жанр.

Идентификаторы структуры не имеют связанных текстовых строк. Когда идентификатор структуры отображается в текстовых данных, он сигнализирует, что следующие текстовые строки применяются к этой логической части DVD-диска вплоть до идентификатора следующей структуры. Расположение идентификаторов структуры в текстовых данных соответствует логической иерархии тома DVD. Например, первое вхождение \_ \_ идентификатора заголовка структуры DVD (0x02) представляет первый заголовок в томе, а следующее вхождение — второй заголовок.

В следующей таблице показано, как можно определить текстовые строки для DVD-диска с двумя заголовками.



| \_ТЕКСТСТРИНГТИПЕ DVD        | Текстовая строка  | Описание                                    |
|----------------------------|--------------|------------------------------------------------|
| \_Том структуры DVD \_ (0x01) | ""           | Идентификатор структуры для всей стороны диска. |
| \_Общее \_ имя DVD (0x30)  | "Том DVD" | Имя тома DVD.                               |
| \_Название структуры DVD \_ (0x02)  | ""           | Идентификатор структуры для первого заголовка.      |
| \_Общее \_ имя DVD (0x30)  | "Заголовок 1"    | Имя первого заголовка.                       |
| \_Название структуры DVD \_ (0x02)  | ""           | Идентификатор структуры для второго заголовка.     |
| \_Общее \_ имя DVD (0x30)  | "Title 2"    | Имя второго заголовка.                      |



 

Методы [**жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) и [**жетдвдтекстстрингаснативе**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) считают идентификаторы структуры и идентификаторы содержимого одинаковыми. Единственное отличие заключается в том, что для идентификаторов структуры связанный текстовый буфер пуст. Приложение следит за взаимоотношениями между текстовыми строками и логическими частями DVD-диска.

В следующем примере показано, как получить текстовые строки с DVD-диска. В этом примере игнорируются некоторые сведения, которые потребуются для реальных приложений. (Например, идентификаторы структуры игнорируются.) Пример предназначен только для отображения правильной последовательности вызовов.


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



Сведения о строках текста DVD см. на [веб-сайте форума на DVD](https://go.microsoft.com/fwlink/?LinkId=8677).

Метод **кдвдкоре:: жетдвдтекст** в приложении двдсампле демонстрирует основные шаги по перечислению и отображению текстовых строк DVD.

## <a name="related-topics"></a>См. также

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> </dl>

 

 



