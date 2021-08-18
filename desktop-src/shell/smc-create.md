---
description: Уведомляет о создании строки меню.
title: Сообщение SMC_CREATE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 537c535d5470a691cf110b2217bb31cbfd0ad78b328f4fbb32a1445e0c5e6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968223"
---
# <a name="smc_create-message"></a>SMC \_ Создание сообщения

Уведомляет о создании строки меню.


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псмд* 
</dt> <dd>

Указатель на элемент **пвусердата** структуры [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .

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



 

 




