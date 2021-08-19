---
description: Указывает, содержит ли поток защищенное содержимое.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Атрибут MF_SD_PROTECTED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ae6cf92b3ada6309de7e92a722db38c88ce94a8af88aa6cc0176f738ff194b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474058"
---
# <a name="mf_sd_protected-attribute"></a>\_Атрибут MF SD \_ protected

Указывает, содержит ли поток защищенное содержимое.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут применяется к дескрипторам потоков. Если значение атрибута равно **true**, поток содержит защищенное содержимое. Если значение равно **false** или атрибут не задан, поток содержит неясное содержимое.

Вместо того чтобы проверять каждый поток для этого атрибута, можно передать дескриптор представления в функцию [**мфрекуирепротектеденвиронмент**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) . Эта функция проверяет, содержит ли дескриптор презентации защищенные потоки.

Источник мультимедиа должен установить этот атрибут в дескрипторе потока, если для содержимого требуется защищенный путь к носителю (PMP).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="examples"></a>Примеры


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Атрибуты дескриптора потока](stream-descriptor-attributes.md)
</dt> </dl>

 

 




