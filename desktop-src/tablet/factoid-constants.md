---
description: Определяет константные строковые значения, которые используются для повышения точности распознавания путем предоставления распознаватель контекстной информации.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Константы фактоид (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa748c84f8bd39f18f83e1ec72474bcfbe3017f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883675"
---
# <a name="factoid-constants"></a>Константы фактоид

Определяет константные строковые значения, которые используются для повышения точности распознавания путем предоставления распознаватель контекстной информации.




| Имя | Описание | 
|------|-------------|
| <span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl><dt><strong>FACTOID_NONE</strong></dt></dl> | Отключает все остальные фактоидс и словари.<br /> | 
| <span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl><dt><strong>FACTOID_DEFAULT</strong></dt></dl> | Значение по умолчанию для фактоидс для западных языков включает системный словарь, Пользовательский словарь, различные знаки препинания, а также веб-фактоид и Number. Значение по умолчанию для фактоидс для восточно-азиатских языков включает все символы, поддерживаемые распознавателем. <br /> | 
| <span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl><dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt></dl> | Указывает распознавателю использовать только системный словарь.<br /> | 
| <span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl><dt><strong>FACTOID_WORDLIST</strong></dt></dl> | Указывает распознавателю использовать программный список слов. Список слов определяется свойством <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>"список слов"</strong></a> объекта <a href="inkrecognizercontext-class.md"><strong>инкрекогнизерконтекст</strong></a> . <br /><blockquote>[!Note]<br />Если строка добавляется в список слов, ее заглавные версии также неявно добавляются. Например, при добавлении слова "Hello" неявно добавляются слова "Hello" и "HELLO".</blockquote><br /> | 
| <span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl><dt><strong>FACTOID_EMAIL</strong></dt></dl> | Указывает распознавателю искать адрес электронной почты.<br /><blockquote>[!Note]<br />Для этого фактоид необходимо использовать полный адрес электронной почты, например " someone@example.com ". Один псевдоним, например "кто-нибудь", не распознается.</blockquote><br /><pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre> | 
| <span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl><dt><strong>FACTOID_WEB</strong></dt></dl> | Указывает распознавателю искать веб-адрес.<br /><pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre> | 
| <span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl><dt><strong>FACTOID_ONECHAR</strong></dt></dl> | Указывает распознавателю искать одиночный символ.<br /><blockquote>[!Note]<br />Этот фактоид ищет любой изолированный символ ANSI.</blockquote><br /> | 
| <span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl><dt><strong>FACTOID_NUMBER</strong></dt></dl> | Указывает распознавателю искать число.<br /><blockquote>[!Note]<br />К числовым значениям относятся разделители, десятичные числа, порядковые номера и другие часто используемые числовые символы.</blockquote><br /> | 
| <span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl><dt><strong>FACTOID_DIGIT</strong></dt></dl> | Указывает распознавателю искать одну цифру от 0 до 9.<br /><pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre> | 
| <span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl><dt><strong>FACTOID_NUMBERSIMPLE</strong></dt></dl> | Предоставляет распознаватель с простым числовым контекстом.<br /><blockquote>[!Note]<br />Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</blockquote><br /> | 
| <span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl><dt><strong>FACTOID_CURRENCY</strong></dt></dl> | Указывает распознавателю искать символы, обозначающие денежные значения.<br /><pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre> | 
| <span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl><dt><strong>FACTOID_POSTALCODE</strong></dt></dl> | Указывает распознавателю искать почтовые коды.<br /><pre class="syntax" data-space="preserve"><code>98112</code></pre> | 
| <span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl><dt><strong>FACTOID_PERCENT</strong></dt></dl> | Указывает распознавателю искать проценты.<br /><pre class="syntax" data-space="preserve"><code>87%</code></pre> | 
| <span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl><dt><strong>FACTOID_DATE</strong></dt></dl> | Указывает распознавателю искать символы, которые обозначают дату.<br /><pre class="syntax" data-space="preserve"><code>10/30/2001, '01, 31/12, 12/99, 1999-2000</code></pre> | 
| <span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl><dt><strong>FACTOID_TIME</strong></dt></dl> | Указывает распознавателю искать символы, которые обозначают время.<br /><pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre> | 
| <span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl><dt><strong>FACTOID_TELEPHONE</strong></dt></dl> | Указывает распознавателю искать символы, которые обозначают номер телефона.<br /><pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre> | 
| <span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl><dt><strong>FACTOID_FILENAME</strong></dt></dl> | Указывает распознавателю искать символы, которые обозначают имя файла.<br /><pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre> | 
| <span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl><dt><strong>FACTOID_UPPERCHAR</strong></dt></dl> | Указывает распознавателю искать один символ в верхнем регистре: от A до Z.<br /> | 
| <span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl><dt><strong>FACTOID_LOWERCHAR</strong></dt></dl> | Указывает распознавателю искать один символ в нижнем регистре: от A до Z.<br /><blockquote>[!Note]<br />Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</blockquote><br /> | 
| <span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl><dt><strong>FACTOID_PUNCCHAR</strong></dt></dl> | Указывает распознавателю искать символы пунктуации.<br /><blockquote>[!Note]<br />Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</blockquote><br /> | 
| <span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl><dt><strong>FACTOID_JAPANESECOMMON</strong></dt></dl> | Указывает распознавателю искать часто используемые символы кандзи, катакана и хирагана.<br /> | 
| <span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl><dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt></dl> | Указывает распознавателю искать часто используемые символы упрощенного китайского письма.<br /> | 
| <span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl><dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt></dl> | Указывает распознавателю искать часто используемые символы традиционного китайского языка.<br /> | 
| <span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl><dt><strong>FACTOID_KOREANCOMMON</strong></dt></dl> | Указывает распознавателю искать часто используемые корейские символы.<br /> | 
| <span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl><dt><strong>FACTOID_HIRAGANA</strong></dt></dl> | Указывает распознавателю искать только символы хирагана.<br /> | 
| <span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl><dt><strong>FACTOID_KATAKANA</strong></dt></dl> | Указывает распознавателю искать только символы катакана.<br /> | 
| <span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl><dt><strong>FACTOID_KANJICOMMON</strong></dt></dl> | Указывает распознавателю искать часто используемые символы кандзи.<br /> | 
| <span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl><dt><strong>FACTOID_KANJIRARE</strong></dt></dl> | Указывает распознавателю искать редко используемые символы кандзи.<br /><blockquote>[!Note]<br />Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</blockquote><br /> | 
| <span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl><dt><strong>FACTOID_BOPOMOFO</strong></dt></dl> | Указывает распознавателю искать бопомофо-символы.<br /> | 
| <span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl><dt><strong>FACTOID_JAMO</strong></dt></dl> | Указывает распознавателю искать символы азбуки хангыль-совместимости.<br /> | 
| <span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl><dt><strong>FACTOID_HANGULCOMMON</strong></dt></dl> | Указывает распознавателю искать часто используемые символы хангыль.<br /> | 
| <span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl><dt><strong>FACTOID_HANGULRARE</strong></dt></dl> | Указывает распознавателю искать редко используемые символы хангыль.<br /><blockquote>[!Note]<br />Эта фактоид не поддерживается в этой версии пакета SDK для планшетных ПК.</blockquote><br /> | 




## <a name="remarks"></a>Комментарии

В C++ вы можете получить доступ к этим константам в файле заголовка Мсинкаут. h, который находится в папке &lt; systemdrive &gt; : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include, если пакет SDK установлен в расположение по умолчанию.

> [!Note]  
> Эти константы являются Вчарс, а не BSTRs. Перед использованием в качестве параметров методов объекта их необходимо преобразовать в BSTRs. Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).

 

> [!Note]  
> Для распознавания символов латинского алфавита фактоидс, определенный в этом классе, предоставляется только для обратной совместимости. Для новой разработки рекомендуется использовать значения, определенные в функции [сетинпутскопе](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) . Дополнительные сведения см. [в разделе Использование контекста для повышения точности](using-context-to-improve-accuracy.md).

 

Используйте эти идентификаторы, чтобы указать, какие фактоид должны использоваться во время распознавания.

Следующие сочетания фактоидс поддерживаются только для западных языков. Они не имеют отдельных определений, но являются допустимыми входными строковыми литералами для свойства [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) объектов, использующих фактоидс. Эти константы фактоид строк позволяют входным данным соответствовать любому из фактоидс в выражении.



| Сочетание               | Определение                                                |
|---------------------------|-----------------------------------------------------------|
| "веб- \| список слов"           | Веб-фактоид или список слов.                         |
| " \| список слов электронной почты"         | Фактоид электронной почты или список слов.                       |
| "имя_файла \| Web \| список слов" | Имя файла фактоид или веб-фактоид или список слов. |



 

Если используется элемент управления [InkEdit](inkedit-control-reference.md) , фактоид может быть задан как свойство элемента управления.

При использовании API платформы Tablet PC можно задать свойство [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) для объекта [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) .

Кроме того, можно задать для этого свойства фактическую строковую константу фактоид.

> [!Note]  
> Константы строк фактоид чувствительны к регистру. Дополнительные сведения о фактоидс и способах их использования см. в разделе Использование контекста для [повышения точности](using-context-to-improve-accuracy.md). Чтобы определить, доступен ли фактоид на определенном языке, см. раздел [Supported фактоидс from версии 1](supported-factoids-from-version-1.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс фактоид свойства \[ инкрекогнизеконтекст\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Класс фактоид свойства \[ пенинпутпанел\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**\[Элемент управления InkEdit свойства фактоид\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Использование контекста для повышения точности](using-context-to-improve-accuracy.md)
</dt> <dt>

[Поддерживаемые Фактоидс из версии 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

