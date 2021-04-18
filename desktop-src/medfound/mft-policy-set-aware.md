---
description: Указывает, требуется ли Имфтрансформ получать уведомления о завершении Меполицисет.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719464"
---
# <a name="mft_policy_set_aware-attribute"></a>\_Атрибут с \_ поддержкой набора политик \_ MFT

Если значение не равно нулю, указывает, что **имфтрансформ** хочет получать уведомления о завершении [меполицисет](./mepolicyset.md) .

## <a name="data-type"></a>Тип данных

**UINT32** (рассматривается как **bool**)

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имфинпуттрустаусорити**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>Комментарии

Этот атрибут может использоваться средством расшифровки **имфинпуттрустаусорити** . Реализация модуля расшифровки содержимого (CDM) может включать реализацию **имфинпуттрустаусорити**. Доступ к объекту **имфинпуттрустаусорити** осуществляется через [Имфконтентдекриптионмодуле:: креатетрустединпут](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).


Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Обновление Windows 10 от апреля 2020   <br/>                                        |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 
