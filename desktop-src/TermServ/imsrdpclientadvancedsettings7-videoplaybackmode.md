---
title: IMsRdpClientAdvancedSettings7 Видеоплайбаккмоде, свойство
description: Указывает или получает значение, указывающее режим воспроизведения видео.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Видеоплайбаккмоде
- Службы удаленных рабочих столов свойства Видеоплайбаккмоде, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Видеоплайбаккмоде
- Службы удаленных рабочих столов свойства Видеоплайбаккмоде, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Видеоплайбаккмоде
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cf72822ac91686cb5a08edf5ca6a5e25b24ff8e544ff79bdd8a2085f761fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607821"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>Свойство IMsRdpClientAdvancedSettings7:: Видеоплайбаккмоде

Указывает или получает значение, указывающее режим воспроизведения видео.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>Значение свойства

Значение, указывающее режим воспроизведения видео.

Допустимые значения:

<dt>

1
</dt> <dd>

Режим воспроизведения видео по умолчанию. Если для режима воспроизведения видео задано это значение, перенаправление видео управляется свойством [**аудиоредиректионмоде**](imsrdpclientsecuredsettings-autoredirectionmode.md) . Если для свойства **аудиоредиректионмоде** задано **\_ \_ перенаправление в звуковом режиме**, видео декодировано и отображается на клиенте.

</dd> <dt>

0
</dt> <dd>

Перенаправление воспроизведения видео отключено, даже если для [**аудиоредиректионмоде**](imsrdpclientsecuredsettings-autoredirectionmode.md) задано **\_ \_ перенаправление в звуковом режиме**. В этом режиме видео декодировано и отображается на сервере узла сеансов удаленных рабочих столов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7<br/>                                                                             |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 определен как 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





