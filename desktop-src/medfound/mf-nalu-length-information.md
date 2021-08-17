---
description: Указывает длину Налус в образце. Это большой двоичный объект MF, заданный в сжатых примерах входных данных для декодера H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Атрибут MF_NALU_LENGTH_INFORMATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2020c0086247adda742ce2613045bb3a2004c3b8c13c7cdcb04a0ff3997cf0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104420"
---
# <a name="mf_nalu_length_information-attribute"></a>\_ \_ Атрибут сведений о длине MF налу \_

Указывает длину Налус в образце. Это **большой двоичный объект** MF, заданный в сжатых примерах входных данных для декодера H. 264.

## <a name="data-type"></a>Тип данных

**ОБЪЕКТЕ**

## <a name="remarks"></a>Remarks

Чтобы задать этот атрибут, носитель должен иметь тип МЕДИАСУБТИПЕ \_ H264 Single bitrate, а для входного типа носителя медиасубтипе H264 Single bitrate должен быть задан атрибут [ \_ длины MF налу \_ length \_ ](mf-nalu-length-set.md) \_ .

Задайте \_ \_ сведения о длине MF налу в \_ виде **большого двоичного объекта** в примере входных данных с одним DWORD для каждого налу в образце. Например, если имеется AUD (9 байт), SPS (25 байт), PPS (10 байт), IDR slice1 (50 k), IDR Slice 2 (60 k), то в **BLOB-объекте** должно быть 5 DWORD со значениями 9, 25, 10, 50 k и 60 k.

Ниже приведен код, задающий **большой двоичный объект**, где **ргдвналуленгсинфо** — массив типа DWORD, а **УИНАЛУЛЕНГСИДКС** — допустимая длина налу, установленная для **большого двоичного объекта**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> </dl>

 

 




