---
description: Указывает, является ли поток взаимоисключающим с другими потоками того же типа.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Атрибут MF_SD_MUTUALLY_EXCLUSIVE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712399"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a>\_Атрибут, \_ \_ взаимоисключающий MF SD

Указывает, является ли поток взаимоисключающим с другими потоками того же типа.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфстреамдескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Комментарии

Если этот атрибут имеет **значение true** (отличное от нуля), поток является взаимоисключающим с другими потоками того же типа, например аудио или видео, в той же презентации. Например, если AVI-файл содержит несколько звуковых потоков, они помечаются как взаимоисключающие, так как только один звуковой поток должен воспроизводиться за один раз.

Значение по умолчанию — **false**.

> [!Note]  
> Этот атрибут не используется для файлов ASF, которые имеют более сложный способ представления условий взаимного исключения. Дополнительные сведения см. в разделе [**имфасфмутуалексклусион**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).

 

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты дескриптора потока](stream-descriptor-attributes.md)
</dt> </dl>

 

 




