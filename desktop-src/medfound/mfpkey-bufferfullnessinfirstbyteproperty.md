---
description: Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Свойство MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693604"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>МФПКЭЙ \_ буфферфуллнессинфирстбите, свойство

Указывает, содержит ли закодированный поток видео значение полных буферов со всеми ключевыми кадрами.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвкбуфферфуллнессинфирстбите

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="remarks"></a>Комментарии

Перед получением этого значения необходимо задать выходной тип.

Значение этого свойства можно получить с помощью [ивмкодекпропс:: жеткодекпроп](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). При использовании **ипропертибаг** необходимо сначала задать значение FOURCC нужного сжатого формата с помощью свойства [мфпкэй \_ FourCC](mfpkey-fourccproperty.md) .

Заполнение буфера в первом байте всех ключевых кадров позволяет определить размер буфера, необходимый при объединении сжатых потоков видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




