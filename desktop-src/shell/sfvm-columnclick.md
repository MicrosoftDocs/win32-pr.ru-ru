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
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497889"
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

## <a name="remarks"></a>Примечания

В ответ на это уведомление следует вернуть \_ "ОК" для самостоятельного изменения списка. Чтобы объект представления системной папки переупорядочивает список, возвратите \_ значение false.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
