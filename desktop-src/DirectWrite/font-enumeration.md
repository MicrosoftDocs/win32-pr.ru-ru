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
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="21707-103">Как перечислить шрифты</span><span class="sxs-lookup"><span data-stu-id="21707-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="21707-104">В этом обзоре будет показано, как перечислить шрифты в коллекции системных шрифтов по имени семейства.</span><span class="sxs-lookup"><span data-stu-id="21707-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="21707-105">Этот обзор состоит из следующих частей.</span><span class="sxs-lookup"><span data-stu-id="21707-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="21707-106">Шаг 1. получение коллекции системных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="21707-107">Шаг 2. Получение числа семейств шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="21707-108">Создайте цикл for.</span><span class="sxs-lookup"><span data-stu-id="21707-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="21707-109">Шаг 3. получение семейства шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="21707-110">Шаг 4. Получение имен семейств.</span><span class="sxs-lookup"><span data-stu-id="21707-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="21707-111">Шаг 5. Поиск имени локали.</span><span class="sxs-lookup"><span data-stu-id="21707-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="21707-112">Шаг 6. Получение длины строки имени семейства и строки.</span><span class="sxs-lookup"><span data-stu-id="21707-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="21707-113">Заключение</span><span class="sxs-lookup"><span data-stu-id="21707-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="21707-114">Пример кода</span><span class="sxs-lookup"><span data-stu-id="21707-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="21707-115">Шаг 1. получение коллекции системных шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="21707-116">Используйте метод [**жетсистемфонтколлектион**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) , предоставленный фабрикой DirectWrite, чтобы вернуть [**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) со всеми системными шрифтами в нем.</span><span class="sxs-lookup"><span data-stu-id="21707-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="21707-117">Шаг 2. Получение числа семейств шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="21707-118">Затем получите число семейств шрифтов из коллекции шрифтов с помощью [**идвритефонтколлектион:: жетфонтфамиликаунт**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span><span class="sxs-lookup"><span data-stu-id="21707-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="21707-119">Мы будем использовать его для циклического перебора каждого семейства шрифтов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="21707-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="21707-120">Создайте цикл for.</span><span class="sxs-lookup"><span data-stu-id="21707-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="21707-121">Теперь, когда у вас есть коллекция шрифтов и число шрифтов, оставшиеся шаги переносятся по каждому семейству шрифтов, извлекают объект [**идвритефонтфамили**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) и запрашивают его.</span><span class="sxs-lookup"><span data-stu-id="21707-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="21707-122">Шаг 3. получение семейства шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="21707-123">Получите объект [**идвритефонтфамили**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) с помощью [**идвритефонтколлектион::-FontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) и передавайте ему текущий индекс, *i*.</span><span class="sxs-lookup"><span data-stu-id="21707-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="21707-124">Шаг 4. Получение имен семейств.</span><span class="sxs-lookup"><span data-stu-id="21707-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="21707-125">Получите имена семейств шрифтов с помощью [**идвритефонтфамили:: жетфамилинамес**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span><span class="sxs-lookup"><span data-stu-id="21707-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="21707-126">Это объект [**идврителокализедстрингс**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) .</span><span class="sxs-lookup"><span data-stu-id="21707-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="21707-127">Он может иметь несколько локализованных версий имени семейства шрифтов.</span><span class="sxs-lookup"><span data-stu-id="21707-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="21707-128">Шаг 5. Поиск имени локали.</span><span class="sxs-lookup"><span data-stu-id="21707-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="21707-129">Получите имя шрифта фамлий в нужном языковом стандарте с помощью метода [**идврителокализедстрингс:: финдлокаленаме**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) .</span><span class="sxs-lookup"><span data-stu-id="21707-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="21707-130">В этом случае сначала извлекается и запрашивается языковой стандарт по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21707-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="21707-131">Если это не сработает, запрашивается языковой стандарт "en-US".</span><span class="sxs-lookup"><span data-stu-id="21707-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="21707-132">Если ни один из указанных языков не найден, этот пример просто возвращается к индексу 0 — первому доступному языку.</span><span class="sxs-lookup"><span data-stu-id="21707-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="21707-133">Шаг 6. Получение длины строки имени семейства и строки.</span><span class="sxs-lookup"><span data-stu-id="21707-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="21707-134">Наконец, получите длину строки имени семейства с помощью [**идврителокализедстрингс:: жетстрингленгс**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span><span class="sxs-lookup"><span data-stu-id="21707-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="21707-135">Используйте эту длину для выделения строки, достаточно большой для хранения имени, а затем получения имени семейства шрифтов с помощью [**идврителокализедстрингс:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span><span class="sxs-lookup"><span data-stu-id="21707-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="21707-136">Заключение</span><span class="sxs-lookup"><span data-stu-id="21707-136">Conclusion</span></span>

<span data-ttu-id="21707-137">Указав имя семейства или имена в языковом стандарте, вы можете перечислить их для пользователя или передать в Креатетекстформат, чтобы начать форматирование текста с указанным семейством шрифтов и т. д.</span><span class="sxs-lookup"><span data-stu-id="21707-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="21707-138">Пример кода</span><span class="sxs-lookup"><span data-stu-id="21707-138">Example Code</span></span>

<span data-ttu-id="21707-139">Полный исходный код для этого примера см. в [примере перечисления шрифтов](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="21707-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 