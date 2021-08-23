---
description: Возвращает значок по умолчанию для элемента, указанного сопутствующей структурой СМДАТА.
title: Сообщение SMC_DEFAULTICON (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c0245cad585f461fbc1b22611b0a39a25ec0e6ac235bb29a490fdd47ba5e5979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968203"
---
# <a name="smc_defaulticon-message"></a>\_Сообщение SMC дефаултикон

Возвращает значок по умолчанию для элемента, указанного сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзикон* 
</dt> <dd>

Указатель на строку, которая получает полный путь к файлу, содержащему значок по умолчанию.

</dd> <dt>

*iIcon* 
</dt> <dd>

Указатель на целое число, которое получает индекс значка в файле, указанном параметром *пвсзикон*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК.

## <a name="remarks"></a>Remarks

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




