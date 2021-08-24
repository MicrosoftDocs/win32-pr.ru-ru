---
description: Указывает список идентификаторов языка, который указывает языки, содержащиеся в файле ASF. Этот атрибут соответствует объекту списка языков, определенному в спецификации ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: Атрибут MF_PD_ASF_LANGLIST (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba22004001df2ba6be8fb7a173a3ea9bed1b0a73863ae111e61d36efa853e079
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119103706"
---
# <a name="mf_pd_asf_langlist-attribute"></a>\_ \_ Атрибут ланглист MF PD ASF \_

Указывает список идентификаторов языка, который указывает языки, содержащиеся в файле ASF. Этот атрибут соответствует объекту списка языков, определенному в спецификации ASF.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам представления для содержимого ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из заголовка объекта списка языков. В следующей таблице показан формат большого двоичного объекта.



| Поле объекта списка языков | Тип данных    | Размер    | Описание                            |
|----------------------------|--------------|---------|----------------------------------------|
| Число записей ИДЕНТИФИКАТОРов языков  | **DWORD**    | 4 байта | Число языков                    |
| Записи идентификатора языка        | **ДВУХБАЙТОВЫХ**\[\] | Различается  | Массив строк языка (см. ниже). |



 

Первый **DWORD** — это число языков, за которым следует массив строк идентификатора языка. Каждая строка имеет следующий формат:



| Поле объекта списка языков | Тип данных     | Размер    | Описание                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Длина идентификатора языка         | **DWORD**     | 4 байта | Длина строки в байтах, включая размер завершающего **нуль** символа. |
| Идентификатор языка                | **WCHAR**\[\] | Различается  | Строка, заканчивающаяся нулем и содержащая имя языка RFC 1766.                           |



 

Каждая строка является тегом языка, совместимым с RFC 1766.

Чтобы получить тег языка для конкретного потока в файле ASF, запросите дескриптор потока для атрибута [**\_ \_ \_ \_ индекса Екстстрмпроп языка ( \_ ИД \_ ) MF SD ASF**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .

## <a name="examples"></a>Примеры

В следующем примере показано, как выполнить синтаксический анализ списка языков.


```C++
class LanguageList
{
private:
    UINT8   *pRawList;          // Unparsed blob
    UINT32  cbList;             // Size of the blob, in bytes
    DWORD   cLangs;             // Number of languages
    WCHAR   **ppszLanguages;    // Array of pointers to strings.
                                // These are pointers into pRawList.
public:
    LanguageList() : 
        pRawList(NULL), cbList(0), ppszLanguages(NULL), cLangs(0)
    {
    }
    ~LanguageList()
    {
        Clear();
    }

    // Clear: Clears the list.
    void Clear()
    {
        CoTaskMemFree(pRawList);
        cbList = 0;
        cLangs = 0;
        delete [] ppszLanguages;

        ppszLanguages = NULL;
    }

    // GetCount: Returns the number of languages.
    DWORD GetCount() const { return cLangs; }

    // GetLanguage: Return the i'th string in the list.
    const WCHAR* GetLanguage(DWORD i)
    {
        if (i >= cLangs)
        {
            return NULL;
        }
        return ppszLanguages[i];
    }

    // Initialize: Get the language list, if specified, and parse it.
    HRESULT Initialize(IMFPresentationDescriptor *pPD)
    {
        if (pPD == NULL)
        {
            return E_POINTER;
        }
        Clear();

        HRESULT hr = pPD->GetAllocatedBlob(
            MF_PD_ASF_LANGLIST, &pRawList, &cbList);

        if (FAILED(hr))
        {
            goto done;
        }


        // Parse the language blob.

        // Record count.
        if (cbList < sizeof(DWORD))
        {
            hr = E_FAIL;
            goto done;
        }

        cLangs = ((DWORD*)pRawList)[0];

        // Allocate an array of pointers to language strings.
        ppszLanguages = new (std::nothrow) WCHAR*[cLangs];
        if (ppszLanguages == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        ZeroMemory(ppszLanguages, cLangs * sizeof(WCHAR*));

        BYTE *pNext = pRawList + sizeof(DWORD); // Next byte.
        BYTE *pEnd = pRawList + cbList;         // End of the blob.

        for (DWORD i = 0; i < cLangs; i++)
        {
            if (pNext > pEnd - sizeof(DWORD))
            {
                hr = E_FAIL;
                goto done;
            }

            // Language ID length
            DWORD cbStr = ((DWORD*)pNext)[0];
            pNext += sizeof(DWORD);

            // Calculate the pointer to the language ID string.
            if ((cbStr > (size_t)(pEnd - pNext)) ||
                (cbStr < sizeof(WCHAR)) || 
                (cbStr % sizeof(WCHAR) != 0))
            {
                hr = E_FAIL;
                goto done;
            }

            ppszLanguages[i] = (WCHAR*)pNext;

            // Verify the string is NULL-terminated.
            if (ppszLanguages[i][(cbStr / sizeof(WCHAR)) - 1] != L'\0')
            {
                hr = E_FAIL;
                goto done;
            }
            pNext += cbStr;
        }

done:
        if (FAILED(hr))
        {
            Clear();
        }

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // There was no language list attribute in the PD.
            // This is not a failure case.
            hr = S_OK;  
        }
        return hr;
    }

private:
    LanguageList(const LanguageList& lang);
    LanguageList& operator=(const LanguageList& lang);
};
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> <dt>

Объект заголовка ASF
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> </dl>

 

 




