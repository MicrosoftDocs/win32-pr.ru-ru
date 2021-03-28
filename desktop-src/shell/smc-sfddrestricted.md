---
description: Запрашивает возможность удаления объекта данных в элементе, указанном сопутствующей структурой СМДАТА.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Сообщение SMC_SFDDRESTRICTED (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985733"
---
# <a name="smc_sfddrestricted-message"></a>\_Сообщение SMC сфддрестриктед

Запрашивает возможность удаления объекта данных в элементе, указанном сопутствующей структурой [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдроптаржет* 
</dt> <dd>

Адрес указателя void, который получает указатель на интерфейс [**интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Если вы не хотите принимать объект данных, присвойте этому параметру значение **null** .

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



 

 
