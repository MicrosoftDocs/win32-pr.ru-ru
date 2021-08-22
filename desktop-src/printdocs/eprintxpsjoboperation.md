---
description: Указывает, находится ли задание печати XPS в очереди печати или на этапе отрисовки.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Перечисление Епринткспсжобоператион (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 44f1f7ed80cd1de071633de37c5f0e91e913841388754a65c0194665bd3084de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971543"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Перечисление Епринткспсжобоператион

Указывает, находится ли задание печати XPS в очереди печати или на этапе отрисовки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**кжобпродуктион**
</dt> <dd>

Задание XPS находится в очереди.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**кжобконсумптион**
</dt> <dd>

Идет подготовка задания XPS.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление в основном используется в качестве параметра функции [**репортжобпроцессингпрогресс**](reportjobprocessingprogress.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>винспул. h (включает Windows. h)</dt> </dl> |



 

 




