---
description: Указывает количество несжатых буферов, которые требуются для работы приемника мультимедиа расширенного модуля подготовки видео (Евр).
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Атрибут MF_SA_REQUIRED_SAMPLE_COUNT (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712253"
---
# <a name="mf_sa_required_sample_count-attribute"></a>\_ \_ \_ Атрибут количества выборок для сопоставления MF \_

Указывает количество несжатых буферов, которые требуются для работы приемника мультимедиа расширенного модуля подготовки видео (Евр).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Комментарии

Это атрибут уровня потока. Чтобы получить атрибут из евр, выполните следующие действия.

1.  Вызовите [**имфмедиасинк:: жетстреамсинкбиндекс**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) , чтобы получить приемник потока.
2.  Запросите приемник потока для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

На внутреннем уровне микшер предоставляет этот атрибут для Евр. Чтобы получить атрибут из микшера, вызовите метод [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




