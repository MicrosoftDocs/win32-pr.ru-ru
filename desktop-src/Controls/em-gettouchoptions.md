---
title: Сообщение EM_GETTOUCHOPTIONS (RichEdit. h)
description: Извлекает параметры касания, связанные с элементом управления Rich Edit.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Элементы управления Windows для EM_GETTOUCHOPTIONS сообщений
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
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071863"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ сеттаучоптионс**](em-settouchoptions.md)
</dt> </dl>

 

 





