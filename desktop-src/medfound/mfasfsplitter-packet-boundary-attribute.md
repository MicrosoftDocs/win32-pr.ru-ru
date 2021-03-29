---
description: Указывает, содержит ли буфер начало пакета расширенного системного формата (ASF).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Атрибут MFASFSPLITTER_PACKET_BOUNDARY (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647204"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>\_ \_ Атрибут границы пакета мфасфсплиттер

Указывает, содержит ли буфер начало пакета расширенного системного формата (ASF).

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Если буфер мультимедиа предоставляет интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) через **QueryInterface**, а значение этого атрибута не равно нулю, разделитель ASF рассматривает буфер как начало нового пакета.

Этот атрибут применяется, если для анализа данных ASF используется разделитель ASF. Если данные ASF имеют переменную длину пакетов, необходимо установить этот атрибут для буферов мультимедиа, передаваемых в метод [**имфасфсплиттер::P арседата**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Присвойте атрибуту **значение true** , если в буфере содержится начало нового пакета. Если буфер содержит продолжение предыдущего пакета, присвойте атрибуту **значение false**. Буферы не могут охватывать несколько пакетов.

Для данных ASF с фиксированными размерами пакетов этот атрибут не является обязательным, а буфер может охватывать несколько пакетов.

Обратите внимание, что стандартные реализации [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , предоставляемые Media Foundation, не предоставляют [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Чтобы использовать этот атрибут, необходимо предоставить собственную реализацию **имфмедиабуффер**; Например, путем заключения буферов, возвращаемых функцией [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты ASF](asf-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




