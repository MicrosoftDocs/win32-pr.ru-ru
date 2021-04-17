---
description: 'Версия метода Имфмедиатипехандлер:: Жеткуррентмедиатипе, поддерживающая удаленное взаимодействие.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: Ремотежеткуррентмедиатипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703433"
---
# <a name="remotegetcurrentmediatype"></a>ремотежеткуррентмедиатипе

Версия метода [**имфмедиатипехандлер:: жеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) , поддерживающая удаленное взаимодействие.

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a>Комментарии

Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод. Метод не отображается в таблице vtable для интерфейса. Если [**жеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.

Этот интерфейс доступен на следующих платформах, если установлены распространяемые компоненты пакета SDK Windows Media Format 11.

-   Windows XP с пакетом обновления 2 (SP2) и более поздние версии.
-   Windows XP Media Center Edition 2005 с KB900325 (Windows XP Media Center Edition 2005) и KB925766 (Октябрь 2006 накопительный пакет обновления для Windows XP Media Center Edition).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Мфууид. lib</dt> </dl>                    |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфмедиатипехандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




