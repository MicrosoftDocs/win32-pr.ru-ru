---
description: Указывает, является ли образец носителя первым примером после разрыва в потоке.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: Атрибут MFSampleExtension_Discontinuity (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac76b8e4d220ece7c34277bfac031213c1c042615d7ca48677839e54b77e5da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241084"
---
# <a name="mfsampleextension_discontinuity-attribute"></a>\_Атрибут прекращения мфсампликстенсион

Указывает, является ли образец носителя первым примером после разрыва в потоке.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Этот атрибут применяется к примерам мультимедиа. Если этот атрибут имеет **значение true**, это означает, что в потоке произошло прекращение, и этот пример является первым, который должен появиться после разрыва.

Если этот атрибут не задан, по умолчанию используется значение **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 




