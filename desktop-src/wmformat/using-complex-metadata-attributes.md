---
title: Использование сложных атрибутов метаданных
description: Использование сложных атрибутов метаданных
ms.assetid: 8269efe4-331f-4b4b-b888-66b45c638153
keywords:
- Windows Пакет SDK для формата мультимедиа, атрибуты сложных метаданных
- Расширенный системный формат (ASF), атрибуты сложных метаданных
- ASF (Расширенный системный формат), атрибуты сложных метаданных
- метаданные, сложные атрибуты
- атрибуты сложных метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8245d2fbc07878a73e304cfc573e05e93b605185ece93655dae7a8bdeff0d9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807254"
---
# <a name="using-complex-metadata-attributes"></a>Использование сложных атрибутов метаданных

пакет SDK для Windows Media Format поддерживает сложные атрибуты метаданных, которые являются атрибутами, содержащими значения, представленные структурой. Поскольку все атрибуты должны иметь тип данных, определенный в перечислении [**\_ \_ DATATYPE ВМТ attr**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) , все сложные атрибуты метаданных обрабатываются как **\_ \_ двоичные типы ВМТ**. При написании сложного атрибута приведите указатель к структуре в виде указателя байтов. При извлечении сложного атрибута приведите массив байтов, заданный [**IWMHeaderInfo3:: жетаттрибутебиндексекс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) в качестве соответствующей структуры.

В следующих примерах кода показано, как задать и получить атрибут сложных метаданных. Первая функция добавляет атрибут Text пользователя, вторая функция получает его. Дополнительные сведения об использовании этих примеров см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT AddText(IWMHeaderInfo3* pHeaderInfo, 
                WCHAR* pwszDesc, 
                WCHAR* pwszText, 
                WORD* pwIndex)
{
    HRESULT hr         = S_OK;
    WORD    wIndex     = 0;
    
    WM_USER_TEXT textStruct;
    
    // Populate the text structure.
    textStruct.pwszDescription = pwszDesc;
    textStruct.pwszText = pwszText;

    // Add the attribute.
    hr = pHeaderInfo->AddAttribute(0, 
                                   g_wszWMText, 
                                   &wIndex, 
                                   WMT_TYPE_BINARY, 
                                   0, 
                                   (BYTE*)&textStruct, 
                                   sizeof(WM_USER_TEXT));

    // Pass the index of the text attribute back to the caller.
    if(SUCCEEDED(hr))
    {
        *pwIndex = wIndex;
    }
    
    return hr;
}

HRESULT DisplayText(IWMHeaderInfo3* pHeaderInfo, WORD wIndex)
{
    HRESULT hr = S_OK;

    WCHAR*  pwszName = NULL;
    WORD    cchName  = 0;
    WORD    Language = 0;
    BYTE*   pbValue  = NULL;
    DWORD   cbValue  = 0;
    

    WM_USER_TEXT*     pText    = NULL;
    WMT_ATTR_DATATYPE AttType;

    
    // Find the lengths of the attribute name and value.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            NULL, 
                                            &cchName, 
                                            NULL, 
                                            NULL, 
                                            NULL, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the name and value.
    pwszName = new WCHAR[cchName];
    pbValue  = new BYTE[cbValue];
    
    if(pwszName == NULL || pbValue == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit;
    }

    // Get the attribute.
    hr = pHeaderInfo->GetAttributeByIndexEx(0, 
                                            wIndex, 
                                            pwszName, 
                                            &cchName, 
                                            &AttType, 
                                            &Language, 
                                            pbValue, 
                                            &cbValue);
    GOTO_EXIT_IF_FAILED(hr);

    // Make sure the attribute is WM/Text, as expected.
    if(wcscmp(pwszName, g_wszWMText))
    {
        // Somehow we got the wrong attribute.
        hr = E_UNEXPECTED;
        goto Exit;
    }

    // Set the structure pointer to the retrieved value.
    pText = (WM_USER_TEXT*) pbValue;

    // Print the strings from the structure.
    printf("Description : %S\n", pText->pwszDescription);
    printf("Text        : %S\n", pText->pwszText);

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_ARRAY_DELETE(pbValue);
    return hr;
}

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Работа с метаданными**](working-with-metadata.md)
</dt> </dl>

 

 




