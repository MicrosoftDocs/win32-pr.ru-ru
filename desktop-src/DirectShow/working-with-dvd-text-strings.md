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
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="1a4e2-103">Работа с текстовыми строками DVD</span><span class="sxs-lookup"><span data-stu-id="1a4e2-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="1a4e2-104">Некоторые диски DVD, особенно диски Караоке, могут содержать список текстовых строк, которые дополняют видео-или аудио-содержимое.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="1a4e2-105">Эти текстовые строки содержат метаданные о содержимом, такие как названия песен, имена исполнителей, сведения о жанрах и т. д.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="1a4e2-106">Текстовые строки могут присутствовать на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="1a4e2-107">Эти строки являются необязательными, и многие диски их не используют.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="1a4e2-108">Чтобы получить текстовые строки с DVD-диска, используйте интерфейс [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , предоставляемый [навигатором DVD](dvd-navigator-filter.md).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="1a4e2-109">Для получения текстовых строк не нужно создавать граф воспроизведения DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="1a4e2-110">Можно просто создать DVD-навигатор, задать громкость DVD, а затем вызвать соответствующие методы строки текста:</span><span class="sxs-lookup"><span data-stu-id="1a4e2-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="1a4e2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="1a4e2-111">Method</span></span>                                                                                  | <span data-ttu-id="1a4e2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1a4e2-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a4e2-113">**IDvdInfo2:: Жетдвдтекстнумберофлангуажес**</span><span class="sxs-lookup"><span data-stu-id="1a4e2-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="1a4e2-114">Возвращает число языков, для которых имеются текстовые строки.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="1a4e2-115">**IDvdInfo2:: Жетдвдтекстлангуажеинфо**</span><span class="sxs-lookup"><span data-stu-id="1a4e2-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="1a4e2-116">Возвращает сведения о текстовых строках для одного языка.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="1a4e2-117">**IDvdInfo2:: Жетдвдтекстстрингасуникоде**</span><span class="sxs-lookup"><span data-stu-id="1a4e2-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="1a4e2-118">Возвращает текстовую строку для указанного языка по индексу.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="1a4e2-119">**IDvdInfo2:: Жетдвдтекстстрингаснативе**</span><span class="sxs-lookup"><span data-stu-id="1a4e2-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="1a4e2-120">Возвращает текстовую строку в виде массива необработанных байтов.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="1a4e2-121">Используйте этот метод, если текстовая строка использует кодировку символов, не поддерживаемую [**жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="1a4e2-122">Ниже приведена базовая процедура получения текстовых строк.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="1a4e2-123">Вызовите метод [**IDvdInfo2:: жетдвдтекстнумберофлангуажес**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) , чтобы найти общее число языков, в которых отображаются текстовые строки.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="1a4e2-124">Если это число равно нулю, значит, DVD-диск не содержит текстовых строк.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="1a4e2-125">(Это, вероятно, наиболее распространенный случай.)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="1a4e2-126">Если число языков не меньше одного, вызовите [**IDvdInfo2:: жетдвдтекстлангуажеинфо**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) , чтобы получить сведения о каждом языке.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="1a4e2-127">Язык указывается с помощью индекса.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-127">The language is specified by index.</span></span> <span data-ttu-id="1a4e2-128">Метод возвращает общее количество текстовых строк на этом языке, код локали (**LCID**) для языка и кодировку символов (Unicode или другой).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="1a4e2-129">Текстовые строки DVD могут использовать несколько различных наборов символов. они перечислены в [**\_ перечислении текстчарсет DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="1a4e2-130">Чтобы получить текстовую строку, вызовите метод [**IDvdInfo2:: жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) или [**IDvdInfo2:: жетдвдтекстстрингаснативе**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="1a4e2-131">Первый метод возвращает строку расширенных символов, но не поддерживает каждый набор символов.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="1a4e2-132">Второй метод возвращает массив байтов, содержащий необработанные текстовые данные.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="1a4e2-133">Для обоих методов можно вызвать метод с указателем буфера **null** , чтобы определить размер строки и тип текста.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="1a4e2-134">Затем выделите буфер и снова вызовите метод, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="1a4e2-135">Каждая текстовая строка имеет связанный код идентификатора, который указывает значение текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="1a4e2-136">Идентификатор возвращается в виде значения [**\_ текстстрингтипе DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) .</span><span class="sxs-lookup"><span data-stu-id="1a4e2-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="1a4e2-137">Существует две категории идентификатора: *идентификаторы структуры* и *идентификаторы содержимого*.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="1a4e2-138">Идентификаторы структуры имеют числовые коды в диапазоне 0x00 – 0x02F.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="1a4e2-139">Идентификаторы содержимого имеют диапазон 0x30 и выше.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="1a4e2-140">(Перечисление **\_ текстстрингтипе DVD** определяет подмножество наиболее распространенных идентификаторов, но методы [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) могут возвращать код идентификатора.) Идентификатор структуры описывает логическую часть DVD-диска, например том, заголовок или часть названия (PTT).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="1a4e2-141">Идентификатор содержимого указывает значение конкретной текстовой строки, например название фильма, название песни или жанр.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="1a4e2-142">Идентификаторы структуры не имеют связанных текстовых строк.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="1a4e2-143">Когда идентификатор структуры отображается в текстовых данных, он сигнализирует, что следующие текстовые строки применяются к этой логической части DVD-диска вплоть до идентификатора следующей структуры.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="1a4e2-144">Расположение идентификаторов структуры в текстовых данных соответствует логической иерархии тома DVD.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="1a4e2-145">Например, первое вхождение \_ \_ идентификатора заголовка структуры DVD (0x02) представляет первый заголовок в томе, а следующее вхождение — второй заголовок.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="1a4e2-146">В следующей таблице показано, как можно определить текстовые строки для DVD-диска с двумя заголовками.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="1a4e2-147">\_ТЕКСТСТРИНГТИПЕ DVD</span><span class="sxs-lookup"><span data-stu-id="1a4e2-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="1a4e2-148">Текстовая строка</span><span class="sxs-lookup"><span data-stu-id="1a4e2-148">Text string</span></span>  | <span data-ttu-id="1a4e2-149">Описание</span><span class="sxs-lookup"><span data-stu-id="1a4e2-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="1a4e2-150">\_Том структуры DVD \_ (0x01)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="1a4e2-151">""</span><span class="sxs-lookup"><span data-stu-id="1a4e2-151">""</span></span>           | <span data-ttu-id="1a4e2-152">Идентификатор структуры для всей стороны диска.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="1a4e2-153">\_Общее \_ имя DVD (0x30)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="1a4e2-154">"Том DVD"</span><span class="sxs-lookup"><span data-stu-id="1a4e2-154">"DVD Volume"</span></span> | <span data-ttu-id="1a4e2-155">Имя тома DVD.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="1a4e2-156">\_Название структуры DVD \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="1a4e2-157">""</span><span class="sxs-lookup"><span data-stu-id="1a4e2-157">""</span></span>           | <span data-ttu-id="1a4e2-158">Идентификатор структуры для первого заголовка.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="1a4e2-159">\_Общее \_ имя DVD (0x30)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="1a4e2-160">"Заголовок 1"</span><span class="sxs-lookup"><span data-stu-id="1a4e2-160">"Title 1"</span></span>    | <span data-ttu-id="1a4e2-161">Имя первого заголовка.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="1a4e2-162">\_Название структуры DVD \_ (0x02)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="1a4e2-163">""</span><span class="sxs-lookup"><span data-stu-id="1a4e2-163">""</span></span>           | <span data-ttu-id="1a4e2-164">Идентификатор структуры для второго заголовка.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="1a4e2-165">\_Общее \_ имя DVD (0x30)</span><span class="sxs-lookup"><span data-stu-id="1a4e2-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="1a4e2-166">"Title 2"</span><span class="sxs-lookup"><span data-stu-id="1a4e2-166">"Title 2"</span></span>    | <span data-ttu-id="1a4e2-167">Имя второго заголовка.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="1a4e2-168">Методы [**жетдвдтекстстрингасуникоде**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) и [**жетдвдтекстстрингаснативе**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) считают идентификаторы структуры и идентификаторы содержимого одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="1a4e2-169">Единственное отличие заключается в том, что для идентификаторов структуры связанный текстовый буфер пуст.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="1a4e2-170">Приложение следит за взаимоотношениями между текстовыми строками и логическими частями DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="1a4e2-171">В следующем примере показано, как получить текстовые строки с DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="1a4e2-172">В этом примере игнорируются некоторые сведения, которые потребуются для реальных приложений.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="1a4e2-173">(Например, идентификаторы структуры игнорируются.) Пример предназначен только для отображения правильной последовательности вызовов.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


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



<span data-ttu-id="1a4e2-174">Сведения о строках текста DVD см. на [веб-сайте форума на DVD](https://go.microsoft.com/fwlink/?LinkId=8677).</span><span class="sxs-lookup"><span data-stu-id="1a4e2-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="1a4e2-175">Метод **кдвдкоре:: жетдвдтекст** в приложении двдсампле демонстрирует основные шаги по перечислению и отображению текстовых строк DVD.</span><span class="sxs-lookup"><span data-stu-id="1a4e2-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a4e2-176">См. также</span><span class="sxs-lookup"><span data-stu-id="1a4e2-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a4e2-177">DVD-приложения</span><span class="sxs-lookup"><span data-stu-id="1a4e2-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



