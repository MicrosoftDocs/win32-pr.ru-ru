---
description: Указывает, находится ли кадр видео с чередованием или с последовательной разверткой.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Атрибут MFSampleExtension_Interlaced (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719424"
---
# <a name="mfsampleextension_interlaced-attribute"></a>Мфсампликстенсион \_ чередующийся атрибут

Указывает, находится ли кадр видео с чередованием или с последовательной разверткой. **Значение true** показывает, что кадр является чередованием. Если **значение равно false**, кадр является прогрессивным. Если не задано, тип носителя описывает чересстрочную развертку. Этот атрибут применяется к примерам мультимедиа.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Комментарии

Для видеосодержимого, содержащего смешанные прогрессивные и чередующиеся кадры, задайте тип мультимедиа с чередованием и используйте этот атрибут в каждом кадре, чтобы указать, является ли кадр прогрессивным или чередованием.

Для содержимого видео, которое полностью перемещается в чередование, задайте тип мультимедиа с чередованием и опустите этот атрибут или задайте для него **значение true** при каждом выборке.

Для содержимого видео, которое полностью прогрессивно, установите для типа мультимедиа значение прогрессивный и пропустите этот атрибут или задайте для него **значение false** в каждом образце.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> <dt>

[Чередование видео](video-interlacing.md)
</dt> </dl>

 

 




