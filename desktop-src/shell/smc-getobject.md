---
description: SMC_GETOBJECT сообщение — запрашивает указатель на указанный объект.
title: Сообщение SMC_GETOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100442"
---
# <a name="smc_getobject-message"></a>\_Сообщение SMC GetObject

Запрашивает указатель на указанный объект.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*IID* 
</dt> <dd>

IID, связанный с запрошенным объектом.

</dd> <dt>

*PV* 
</dt> <dd>

Указатель void, получающий указатель на запрошенный интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК.

## <a name="remarks"></a>Remarks

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) . Создайте запрошенный объект и присвойте указатель на запрашиваемый интерфейс *ПС*.

Могут быть запрошены следующие интерфейсы.

-   [**ишеллмену**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [**ишеллменукаллбакк**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [**Интерфейс IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
