---
title: Сообщение MM_MCISIGNAL (Ммсистем. h)
description: '\_Сообщение МЦИСИГНАЛ mm отправляется в окно для уведомления приложения о том, что устройство MCI достигло места, определенного в предыдущей команде сигнала (MCI \_ Signal).'
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- сообщение MM_MCISIGNAL Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb54b56d35ad34d10d95c2a34b52b370fb856d9c958dd42223c7f0a08ddbdfb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807444"
---
# <a name="mm_mcisignal-message"></a>MM \_ мЦисигнал, сообщение

Сообщение **\_ мЦисигнал mm** отправляется в окно для уведомления приложения о том, что устройство MCI достигло места, определенного в предыдущей команде [**сигнала**](signal.md) ( [**MCI \_ Signal**](mci-signal.md)).


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*
</dt> <dd>

Идентификатор устройства, запускающего сигнальное сообщение.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*лусерпарм*
</dt> <dd>

Значение, передаваемое в **двусерпарм** элемент структуры **\_ \_ \_ параметров сигнала MCI ДГВ** , когда команда **сигнала** определила эту функцию обратного вызова. Кроме того, в нем может содержаться значение расположения.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Сообщения MCI](mci-messages.md)
</dt> <dt>

[**имел**](signal.md)
</dt> </dl>

 

 





