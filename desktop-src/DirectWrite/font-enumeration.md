---
title: Как перечислить шрифты
description: В этом обзоре будет показано, как перечислить шрифты в коллекции системных шрифтов по имени семейства.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413249"
---
# <a name="how-to-enumerate-fonts"></a>Как перечислить шрифты

В этом обзоре будет показано, как перечислить шрифты в коллекции системных шрифтов по имени семейства.

Этот обзор состоит из следующих частей.

-   [Шаг 1. получение коллекции системных шрифтов.](#step-1-get-the-system-font-collection)
-   [Шаг 2. Получение числа семейств шрифтов.](#step-2-get-the-font-family-count)
-   [Создайте цикл for.](#make-a-for-loop)
    -   [Шаг 3. получение семейства шрифтов.](#step-3-get-the-font-family)
    -   [Шаг 4. Получение имен семейств.](#step-4-get-the-family-names)
    -   [Шаг 5. Поиск имени локали.](#step-5-find-the-locale-name)
    -   [Шаг 6. Получение длины строки имени семейства и строки.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Заключение](#conclusion)
-   [Пример кода](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Шаг 1. получение коллекции системных шрифтов.

Используйте метод [**жетсистемфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) , предоставленный фабрикой DirectWrite, чтобы вернуть [**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) со всеми системными шрифтами в нем.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Шаг 2. Получение числа семейств шрифтов.

Затем получите число семейств шрифтов из коллекции шрифтов с помощью [**идвритефонтколлектион:: жетфонтфамиликаунт**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount). Мы будем использовать его для циклического перебора каждого семейства шрифтов в коллекции.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Создайте цикл for.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Теперь, когда у вас есть коллекция шрифтов и число шрифтов, оставшиеся шаги переносятся по каждому семейству шрифтов, извлекают объект [**идвритефонтфамили**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) и запрашивают его.

### <a name="step-3-get-the-font-family"></a>Шаг 3. получение семейства шрифтов.

Получите объект [**идвритефонтфамили**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) с помощью [**идвритефонтколлектион::-FontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) и передавайте ему текущий индекс, *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Шаг 4. Получение имен семейств.

Получите имена семейств шрифтов с помощью [**идвритефонтфамили:: жетфамилинамес**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Это объект [**идврителокализедстрингс**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) . Он может иметь несколько локализованных версий имени семейства шрифтов.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Шаг 5. Поиск имени локали.

Получите имя шрифта фамлий в нужном языковом стандарте с помощью метода [**идврителокализедстрингс:: финдлокаленаме**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) . В этом случае сначала извлекается и запрашивается языковой стандарт по умолчанию. Если это не сработает, запрашивается языковой стандарт "en-US". Если ни один из указанных языков не найден, этот пример просто возвращается к индексу 0 — первому доступному языку.


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>Шаг 6. Получение длины строки имени семейства и строки.

Наконец, получите длину строки имени семейства с помощью [**идврителокализедстрингс:: жетстрингленгс**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Используйте эту длину для выделения строки, достаточно большой для хранения имени, а затем получения имени семейства шрифтов с помощью [**идврителокализедстрингс:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a>Заключение

Указав имя семейства или имена в языковом стандарте, вы можете перечислить их для пользователя или передать в Креатетекстформат, чтобы начать форматирование текста с указанным семейством шрифтов и т. д.

## <a name="example-code"></a>Пример кода

Полный исходный код для этого примера см. в [примере перечисления шрифтов](/samples/browse/?redirectedfrom=MSDN-samples).

 

 