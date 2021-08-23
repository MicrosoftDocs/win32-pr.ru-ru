---
description: 'Уведомляет объект обратного вызова о том, что пользователь щелкнул заголовок столбца, чтобы отсортировать список объектов в представлении папки. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_COLUMNCLICK (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5ebd98ebc887d26bcee4799ffa3412df803fd0dfa099ac41bc69e1c25d83f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592704"
---
# <a name="sfvm_columnclick-message"></a>\_Сообщение сфвм колумнкликк

Уведомляет объект обратного вызова о том, что пользователь щелкнул заголовок столбца, чтобы отсортировать список объектов в представлении папки. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*иколумн* \[ окне\]
</dt> <dd>

Индекс столбца, который был выбран.

</dd> </dl>

## <a name="remarks"></a>Remarks

В ответ на это уведомление следует вернуть \_ "ОК" для самостоятельного изменения списка. Чтобы объект представления системной папки переупорядочивает список, возвратите \_ значение false.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
