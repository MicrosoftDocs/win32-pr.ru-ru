---
title: Сообщение MM_WOM_DONE (Ммсистем. h)
description: Сообщение о \_ \_ завершении вом mm отправляется в окно, когда заданный выходной буфер возвращается приложению. Буферы возвращаются в приложение, когда они воспроизводятся, или в результате вызова функции Вавеаутресет.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- сообщение MM_WOM_DONE Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225ba32f780831ab8b40f487a312a940219abc2e976be75a4e903648344afc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065464"
---
# <a name="mm_wom_done-message"></a>\_Сообщение о \_ завершении вом mm

Сообщение **о \_ \_ завершении вом mm** отправляется в окно, когда заданный выходной буфер возвращается приложению. Буферы возвращаются в приложение, когда они воспроизводятся, или в результате вызова функции [**вавеаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*хаутпутдев*
</dt> <dd>

Маркер устройства вывода аудио аудио, который воспроизводил буфер.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*лпввхдр*
</dt> <dd>

Указатель на структуру [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющую буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Звуковая волна](waveform-audio.md)
</dt> <dt>

[Сообщения волны](waveform-messages.md)
</dt> </dl>

 

