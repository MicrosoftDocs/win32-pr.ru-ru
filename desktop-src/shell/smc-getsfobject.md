---
description: SMC_GETSFOBJECT сообщение — запрашивает указатель на указанный объект.
title: Сообщение SMC_GETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086612"
---
# <a name="smc_getsfobject-message"></a>\_Сообщение SMC жетсфобжект

Запрашивает указатель на указанный объект.


```C++
SMC_GETSFOBJECT 
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

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) . Он аналогичен [**SMC \_ GetObject**](smc-getobject.md) , но используется для элементов папки оболочки. Создайте запрошенный объект и присвойте указатель на запрашиваемый интерфейс *ПС*.

Могут быть запрошены следующие интерфейсы.

-   [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)
-   [**ишеллмену**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**ишеллменукаллбакк**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 
