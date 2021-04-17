---
description: Задает использование видео для кодировщика видео.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: Свойство CODECAPI_AVEncVideoUsage (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27568412613702846e99d0ca556cc59cdc4fc77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650466"
---
# <a name="codecapi_avencvideousage-property"></a>КОДЕКАПИ \_ авенквидеаусаже, свойство

Задает использование видео для кодировщика видео.

## <a name="data-type"></a>Тип данных

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеаусаже**

## <a name="remarks"></a>Комментарии

Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).

[Кодекапи \_ Авенквидеотемпораллайеркаунт](codecapi-avencvideotemporallayercount.md), кодекапи \_ Авенквидеаусаже и [кодекапи \_ авенккоммонратеконтролмоде](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) являются статическими свойствами кодировщика. После установки они вступят в силу только после того, как на закрепление выходных данных камеры будет вызван тип набора носителей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

