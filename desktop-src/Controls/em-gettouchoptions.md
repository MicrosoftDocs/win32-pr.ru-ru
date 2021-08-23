---
title: Сообщение EM_GETTOUCHOPTIONS (RichEdit. h)
description: Извлекает параметры касания, связанные с элементом управления Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- элементы управления Windows сообщений EM_GETTOUCHOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4771cd11fd8aaf16925c97a3242918ba8f7b56e4e580a6f3cd70672a134399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799994"
---
# <a name="em_gettouchoptions-message"></a>\_Сообщение ЖЕТТАУЧОПТИОНС EM

Извлекает параметры касания, связанные с элементом управления Rich Edit.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Параметры сенсорного ввода для извлечения. Может быть одним из указанных далее.



| Значение                                                                                                                                                                        | Значение                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ шовхандлес**</dt> </dl>          | Получает значение, указывающее, видимы ли сенсоры касания.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ дисаблехандлес**</dt> </dl> | Получение этого флага не реализовано.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение параметра, заданного параметром *wParam* . Оно не равно нулю, если *wParam* имеет значение **RTO \_ шовхандлес** , а захваты сенсорного ввода видимы; ноль, в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ сеттаучоптионс**](em-settouchoptions.md)
</dt> </dl>

 

 





