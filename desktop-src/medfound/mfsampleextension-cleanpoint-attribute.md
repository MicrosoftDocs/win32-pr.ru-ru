---
description: Указывает, является ли образец точкой доступа случайным образом.
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: Атрибут MFSampleExtension_CleanPoint (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7181c08b19382a6b9d9da0475ec0a7a0522bd132dc10a2da1da4531d631d02d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241501"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a>Мфсампликстенсион \_ клеанпоинт, атрибут

Указывает, является ли образец точкой доступа случайным образом.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarks

Этот атрибут применяется к примерам. Если атрибут имеет **значение true**, то образец является случайной точкой доступа и декодированием, который может начаться из этого примера. В противном случае образец не является случайной точкой доступа.

Если этот атрибут не задан, по умолчанию используется значение **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



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

 

 




