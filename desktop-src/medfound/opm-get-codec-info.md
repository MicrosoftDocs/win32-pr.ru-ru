---
description: Возвращает значение неустановленного аппаратного кодека.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263507"
---
# <a name="opm_get_codec_info"></a>ОПМ \_ получить \_ \_ сведения о кодека

Возвращает значение неустановленного аппаратного кодека.



| Требование | Значение |
|--------------|-------------------------------------------------------------------------------------------|
| GUID запроса | **ОПМ \_ получить \_ \_ сведения о кодека**                                                                 |
| Входные данные   | Структура [**\_ \_ \_ \_ параметров получения кодека ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Возвращать данные  | Структура [**\_ \_ \_ \_ сведений о кодека ОПМ Get**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Комментарии

Хотя эта команда использует интерфейс [Output Protection Manager](output-protection-manager.md) (ОПМ), она применяется только к аппаратным кодировщикам и декодерам. Он не применяется к устройствам вывода видео.

Как правило, эту команду не следует использовать напрямую. Чтобы получить ценность для аппаратного кодека, вызовите функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) . Эта функция выполняет все вызовы ОПМ, необходимые для отправки команды **ОПМ \_ Get \_ кодек \_ info** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                          |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                             |
| Header<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Запросы состояния ОПМ](opm-status-requests.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> <dt>

[**Иопмвидеуутпут:: о.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




