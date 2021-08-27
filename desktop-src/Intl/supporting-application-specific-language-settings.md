---
description: Приложение может поддерживать другой набор языков интерфейса пользователя, поддерживаемых целевой операционной системой. В этом разделе описывается этот тип поддержки с помощью фрагментов из полных примеров.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: поддержка языков Application-Specific Параметры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c934ea2f01c37eb2f9e846382447a50ccbedcd9b69fe20069216fa46521b02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130064"
---
# <a name="supporting-application-specific-language-settings"></a>поддержка языков Application-Specific Параметры

Приложение может поддерживать другой набор языков интерфейса пользователя, поддерживаемых целевой операционной системой. В этом разделе описывается этот тип поддержки с помощью фрагментов из полных примеров.

## <a name="interpret-users-language-preference"></a>Интерпретировать параметры языка пользователя

Приложение должно сначала определить, какой язык интерфейса пользователя отображать в зависимости от предпочтений пользователя. Код может считывать параметры из файла конфигурации или из параметров реестра.

В следующем примере определяются две функции, используемые для интерпретации настроек языка пользователя. Первая функция иллюстрирует чтение списка языков с разделителями из файла, представленного в коде как "langs.txt". В примере поддерживаются разделители ",", ";"; "." и "". Вторая функция преобразует строку, считанную из файла, в многострочное значение. Эта операция необходима, так как функции многоязыкового интерфейса пользователя, используемые для задания языков, принимают многострочные значения.


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a>Установка языка приложения

После считывания сведений о предпочтениях языка код приложения должен использовать извлеченный параметр, чтобы задать язык приложения. в Windows 7 и более поздних версиях приложение может задать язык на уровне процесса, вызвав функцию [**сетпроцесспреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) .


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



в Windows Vista и более поздних версиях язык приложения задается на уровне потока путем вызова функции [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Настройка языковых настроек приложения](setting-application-language-preferences.md)
</dt> <dt>

[MUI: пример Параметры Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: пример Параметры Application-Specific (до Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



