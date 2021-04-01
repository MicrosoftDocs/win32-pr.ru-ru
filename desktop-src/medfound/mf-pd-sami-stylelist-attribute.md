---
description: Содержит понятные имена для синхронизированных доступных стилей обмена мультимедийными данными (SAMI), определенных в файле SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Атрибут MF_PD_SAMI_STYLELIST (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913164"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>\_ \_ Атрибут стилелист MF PD samid \_

Содержит понятные имена для синхронизированных доступных стилей обмена мультимедийными данными (SAMI), определенных в файле SAMI.

[Источник носителя Sami](sami-media-source.md) задает этот атрибут для создаваемого дескриптора представления.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Большой двоичный объект атрибута имеет следующую структуру:



Тип данных

Описание

Размер (в байтах)

**DWORD**

Число строк стиля.

4

Для каждой строки стиля:

**DWORD**

Размер строки в байтах, включая символ **null** .

4

**LPWSTR**

Строка расширенных символов, заканчивающаяся символом NULL, содержащая имя стиля.

Различается



 

Чтобы задать стиль или получить текущий стиль, используйте интерфейс [**имфсамистиле**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



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

[Источник носителя SAMI](sami-media-source.md)
</dt> </dl>

 

 




