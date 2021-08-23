---
description: Указывает, поврежден ли кадр видео.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: Атрибут MFSampleExtension_FrameCorruption (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d61056e22e9600d3ef2b1270c9d72b46c4b241c3de3f1ba0e74748c3bcb0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603124"
---
# <a name="mfsampleextension_framecorruption-attribute"></a>Мфсампликстенсион \_ фрамекорруптион, атрибут

Указывает, поврежден ли кадр видео.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Видеодекодер может установить этот атрибут для выходных образцов. Если значение равно 1, декодер обнаружил повреждение данных в кадре. Если значение равно 0, данные не повреждены или ничего не обнаружено.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Примеры атрибутов](sample-attributes.md)
</dt> <dt>

[Примеры носителей](media-samples.md)
</dt> </dl>

 

 




