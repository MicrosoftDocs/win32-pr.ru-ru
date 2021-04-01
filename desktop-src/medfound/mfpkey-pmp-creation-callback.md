---
description: Задает обратный вызов, который создает сеанс мультимедиа PMP во время разрешения источника.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Свойство MFPKEY_PMP_Creation_Callback (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263981"
---
# <a name="mfpkey_pmp_creation_callback-property"></a>\_ \_ \_ Свойство обратного вызова создания PMP мфпкэй

Задает обратный вызов, который создает [сеанс мультимедиа PMP](pmp-media-session.md) во время разрешения источника.



Тип данных

Тип ПРОПВАРИАНТ (VT)

ПРОПВАРИАНТ, элемент

**IUnknown \** _

VT \_ Unknown

_ *пунквал**



## <a name="remarks"></a>Комментарии

Для некоторых защищенных содержимого может потребоваться использование этого свойства. Если это так, то процесс разрешения источника завершается ошибкой с кодом ошибки **MF \_ E, \_ \_ требующего \_ \_ \_ обратного вызова при создании PMP**.

Чтобы использовать это свойство, выполните следующие действия.

1.  Вызовите [**пскреатемеморипропертисторе**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) , чтобы создать хранилище свойств.
2.  Реализуйте интерфейс обратного вызова [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
3.  Задайте \_ \_ \_ свойство обратного вызова создания PMP мфпкэй для хранилища свойств. Значение является указателем на реализацию [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Вызовите [**имфсаурцересолвер:: бегинкреатеобжектфромурл**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl). Передайте указатель на хранилище свойств в параметре *ппропс* .

В методе [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) интерфейса ответного вызова выполните следующие действия.

1.  Вызовите [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , чтобы создать [сеанс PMP мультимедиа](pmp-media-session.md).
2.  Вызовите [**имфжетсервице::-Service**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) в сеансе PMP Media, чтобы указатель на интерфейс [**имфпмфост**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .
3.  Вызовите [**имфасинкресулт::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) GetObject для результирующего объекта, который передается в параметре *пасинкресулт* метода [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Запросите возвращенный указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) для интерфейса [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .
4.  Вызовите [**мфпутворкитем**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) со следующими параметрами:
    -   *dwQueue*: **\_ \_ \_ стандартная очередь обратного вызова мфасинк**
    -   *пкаллбакк*: указатель [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , полученный на шаге 3.
    -   *пстате*: указатель [**имфпмфост**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) , полученный на шаге 2.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Сеанс PMP мультимедиа](pmp-media-session.md)
</dt> <dt>

[Путь к защищенному носителю](protected-media-path.md)
</dt> <dt>

[Сопоставитель источников](source-resolver.md)
</dt> </dl>

 

 
