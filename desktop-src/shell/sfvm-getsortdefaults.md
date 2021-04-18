---
description: 'Позволяет объекту обратного вызова указывать параметр сортировки по умолчанию. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETSORTDEFAULTS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986101"
---
# <a name="sfvm_getsortdefaults-message"></a>\_Сообщение сфвм жетсортдефаултс

Позволяет объекту обратного вызова указывать параметр сортировки по умолчанию. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идиректион* \[ заполняет\]
</dt> <dd>

Направление сортировки по умолчанию. Присвойте этому параметру положительное значение для сортировки в возрастающем порядке. Присвойте этому параметру нулевое или отрицательное значение для сортировки в убывающем порядке.

</dd> <dt>

*иколумн* \[ заполняет\]
</dt> <dd>

Столбец, используемый для сортировки. Он будет передан в [**ишеллфолдер:: компареидс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) в младших 16 битах значения *lParam* .

</dd> </dl>

## <a name="remarks"></a>Примечания

> [!Note]  
> : **Сфвм \_ жетсортдефаултс** не распознается объектом представления системных папок.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
