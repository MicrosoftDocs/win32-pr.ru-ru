---
description: Указывает список идентификаторов языка, который указывает языки, содержащиеся в файле ASF. Этот атрибут соответствует объекту списка языков, определенному в спецификации ASF.
ms.assetid: 07b8a991-b392-47c1-a6d7-a1f5dcc82e5c
title: Атрибут MF_PD_ASF_LANGLIST (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecac5eac178c7fb315e0ca4cfdbd540a27eeac28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683876"
---
# <a name="mf_pd_asf_langlist-attribute"></a><span data-ttu-id="9fd21-104">\_ \_ Атрибут ланглист MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="9fd21-104">MF\_PD\_ASF\_LANGLIST attribute</span></span>

<span data-ttu-id="9fd21-105">Указывает список идентификаторов языка, который указывает языки, содержащиеся в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="9fd21-105">Specifies a list of language identifiers which specifies the languages contained in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="9fd21-106">Этот атрибут соответствует объекту списка языков, определенному в спецификации ASF.</span><span class="sxs-lookup"><span data-stu-id="9fd21-106">This attribute corresponds to the Language List Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="9fd21-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9fd21-107">Data type</span></span>

<span data-ttu-id="9fd21-108">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="9fd21-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="9fd21-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9fd21-109">Remarks</span></span>

<span data-ttu-id="9fd21-110">Этот атрибут применяется к дескрипторам представления для содержимого ASF.</span><span class="sxs-lookup"><span data-stu-id="9fd21-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="9fd21-111">Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из заголовка объекта списка языков.</span><span class="sxs-lookup"><span data-stu-id="9fd21-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Language List Object header.</span></span> <span data-ttu-id="9fd21-112">В следующей таблице показан формат большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="9fd21-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="9fd21-113">Поле объекта списка языков</span><span class="sxs-lookup"><span data-stu-id="9fd21-113">Language List Object field</span></span> | <span data-ttu-id="9fd21-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9fd21-114">Data type</span></span>    | <span data-ttu-id="9fd21-115">Размер</span><span class="sxs-lookup"><span data-stu-id="9fd21-115">Size</span></span>    | <span data-ttu-id="9fd21-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9fd21-116">Description</span></span>                            |
|----------------------------|--------------|---------|----------------------------------------|
| <span data-ttu-id="9fd21-117">Число записей ИДЕНТИФИКАТОРов языков</span><span class="sxs-lookup"><span data-stu-id="9fd21-117">Language ID Records Count</span></span>  | <span data-ttu-id="9fd21-118">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9fd21-118">**DWORD**</span></span>    | <span data-ttu-id="9fd21-119">4 байта</span><span class="sxs-lookup"><span data-stu-id="9fd21-119">4 bytes</span></span> | <span data-ttu-id="9fd21-120">Число языков</span><span class="sxs-lookup"><span data-stu-id="9fd21-120">Number of languages</span></span>                    |
| <span data-ttu-id="9fd21-121">Записи идентификатора языка</span><span class="sxs-lookup"><span data-stu-id="9fd21-121">Language ID Records</span></span>        | <span data-ttu-id="9fd21-122">**ДВУХБАЙТОВЫХ**\[\]</span><span class="sxs-lookup"><span data-stu-id="9fd21-122">**BYTE**\[\]</span></span> | <span data-ttu-id="9fd21-123">Различается</span><span class="sxs-lookup"><span data-stu-id="9fd21-123">Varies</span></span>  | <span data-ttu-id="9fd21-124">Массив строк языка (см. ниже).</span><span class="sxs-lookup"><span data-stu-id="9fd21-124">Array of language strings (see below).</span></span> |



 

<span data-ttu-id="9fd21-125">Первый **DWORD** — это число языков, за которым следует массив строк идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="9fd21-125">The first **DWORD** is the number of languages, followed by an array of language identifier strings.</span></span> <span data-ttu-id="9fd21-126">Каждая строка имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="9fd21-126">Each string has the following format:</span></span>



| <span data-ttu-id="9fd21-127">Поле объекта списка языков</span><span class="sxs-lookup"><span data-stu-id="9fd21-127">Language List Object field</span></span> | <span data-ttu-id="9fd21-128">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9fd21-128">Data type</span></span>     | <span data-ttu-id="9fd21-129">Размер</span><span class="sxs-lookup"><span data-stu-id="9fd21-129">Size</span></span>    | <span data-ttu-id="9fd21-130">Описание</span><span class="sxs-lookup"><span data-stu-id="9fd21-130">Description</span></span>                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd21-131">Длина идентификатора языка</span><span class="sxs-lookup"><span data-stu-id="9fd21-131">Language ID Length</span></span>         | <span data-ttu-id="9fd21-132">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="9fd21-132">**DWORD**</span></span>     | <span data-ttu-id="9fd21-133">4 байта</span><span class="sxs-lookup"><span data-stu-id="9fd21-133">4 bytes</span></span> | <span data-ttu-id="9fd21-134">Длина строки в байтах, включая размер завершающего **нуль** символа.</span><span class="sxs-lookup"><span data-stu-id="9fd21-134">The length of the string in bytes, including the size of the trailing **NULL** character.</span></span> |
| <span data-ttu-id="9fd21-135">Идентификатор языка</span><span class="sxs-lookup"><span data-stu-id="9fd21-135">Language ID</span></span>                | <span data-ttu-id="9fd21-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="9fd21-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="9fd21-137">Различается</span><span class="sxs-lookup"><span data-stu-id="9fd21-137">Varies</span></span>  | <span data-ttu-id="9fd21-138">Строка, заканчивающаяся нулем и содержащая имя языка RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="9fd21-138">A null-terminated string containing the RFC 1766 language name.</span></span>                           |



 

<span data-ttu-id="9fd21-139">Каждая строка является тегом языка, совместимым с RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="9fd21-139">Each string is a language tag compliant with RFC 1766.</span></span>

<span data-ttu-id="9fd21-140">Чтобы получить тег языка для конкретного потока в файле ASF, запросите дескриптор потока для атрибута [**\_ \_ \_ \_ индекса Екстстрмпроп языка ( \_ ИД \_ ) MF SD ASF**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="9fd21-140">To get the language tag for a particular stream in the ASF file, query the stream descriptor for the [**MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="9fd21-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="9fd21-141">Examples</span></span>

<span data-ttu-id="9fd21-142">В следующем примере показано, как выполнить синтаксический анализ списка языков.</span><span class="sxs-lookup"><span data-stu-id="9fd21-142">The following example shows how to parse the language list.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="9fd21-143">Требования</span><span class="sxs-lookup"><span data-stu-id="9fd21-143">Requirements</span></span>



| <span data-ttu-id="9fd21-144">Требование</span><span class="sxs-lookup"><span data-stu-id="9fd21-144">Requirement</span></span> | <span data-ttu-id="9fd21-145">Значение</span><span class="sxs-lookup"><span data-stu-id="9fd21-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd21-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9fd21-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd21-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fd21-147">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9fd21-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9fd21-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd21-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9fd21-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9fd21-150">Header</span><span class="sxs-lookup"><span data-stu-id="9fd21-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd21-151"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd21-151"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd21-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fd21-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd21-153">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fd21-153">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9fd21-154">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="9fd21-154">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="9fd21-155">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="9fd21-155">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="9fd21-156">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="9fd21-156">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="9fd21-157">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="9fd21-157">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="9fd21-158">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="9fd21-158">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

<span data-ttu-id="9fd21-159">Объект заголовка ASF</span><span class="sxs-lookup"><span data-stu-id="9fd21-159">ASF Header Object</span></span>
</dt> <dt>

[<span data-ttu-id="9fd21-160">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="9fd21-160">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




