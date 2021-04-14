---
description: Уведомляет о том, что произошло изменение.
title: Сообщение SMC_SHCHANGENOTIFY (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 258a885ddaf61b45df1cfff9f9c77ce37a233dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985561"
---
# <a name="smc_shchangenotify-message"></a>\_Сообщение SMC шчанженотифи

Уведомляет о том, что произошло изменение.


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псмк* 
</dt> <dd>

Указатель на структуру [**смкшчанженотифиструкт**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) со сведениями об изменении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК.

## <a name="remarks"></a>Примечания

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




