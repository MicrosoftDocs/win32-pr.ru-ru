---
description: Уведомляет о том, что всплывающая подсказка будет отображаться для шеврона, связанного с элементом, указанным в сопровождающей структуре СМДАТА.
title: Сообщение SMC_DISPLAYCHEVRONTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497883"
---
# <a name="smc_displaychevrontip-message"></a>\_Сообщение SMC дисплайчевронтип

Уведомляет о том, что всплывающая подсказка будет отображаться для шеврона, связанного с элементом, указанным в сопровождающей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Параметры

Это сообщение не содержит параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК, чтобы отобразить всплывающую подсказку. Возвращает \_ значение false, чтобы предотвратить отображение подсказки.

## <a name="remarks"></a>Примечания

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




