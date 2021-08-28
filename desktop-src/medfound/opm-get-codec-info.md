---
description: Возвращает значение неустановленного аппаратного кодека.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847984"
---
# <a name="opm_get_codec_info"></a>ОПМ \_ получить \_ \_ сведения о кодека

Возвращает значение неустановленного аппаратного кодека.



| Требование | Значение |
|--------------|-------------------------------------------------------------------------------------------|
| GUID запроса | **ОПМ \_ получить \_ \_ сведения о кодека**                                                                 |
| Входные данные   | Структура [**\_ \_ \_ \_ параметров получения кодека ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Возвращать данные  | Структура [**\_ \_ \_ \_ сведений о кодека ОПМ Get**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Remarks

Хотя эта команда использует интерфейс [Output Protection Manager](output-protection-manager.md) (ОПМ), она применяется только к аппаратным кодировщикам и декодерам. Он не применяется к устройствам вывода видео.

Как правило, эту команду не следует использовать напрямую. Чтобы получить ценность для аппаратного кодека, вызовите функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) . Эта функция выполняет все вызовы ОПМ, необходимые для отправки команды **ОПМ \_ Get \_ кодек \_ info** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Запросы состояния ОПМ](opm-status-requests.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> <dt>

[**Иопмвидеуутпут:: о.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




