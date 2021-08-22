---
description: Указывает, когда преобразование очищается.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Атрибут MF_TOPONODE_FLUSH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67e02c297efa68c6e6c585837675a46b729ec2382be072828059fd795d1c67a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663884"
---
# <a name="mf_toponode_flush-attribute"></a>\_ \_ Атрибут записи на диск MF топоноде

Указывает, когда преобразование очищается.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="remarks"></a>Remarks

Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).

Значение атрибута является членом перечисления в [**\_ \_ \_ режиме записи MF топоноде Flush**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) . Если этот атрибут не задан, по умолчанию используется значение **MF \_ топоноде \_ flush \_ Always**.

Очистка выполняется путем вызова [**имфтрансформ::P роцессмессаже**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) в преобразовании с сообщением о [**\_ \_ команде \_ очистки сообщения MFT**](mft-message-command-flush.md) . Дополнительные сведения см. в статье перечисление [**\_ \_ типов сообщений MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




