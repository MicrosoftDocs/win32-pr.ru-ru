---
description: 'Позволяет объекту обратного вызова предоставить страницу для добавления в страницу свойств выбранного объекта. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_ADDPROPERTYPAGES (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997810"
---
# <a name="sfvm_addpropertypages-message"></a>\_Сообщение сфвм аддпропертипажес

Позволяет объекту обратного вызова предоставить страницу для **добавления в страницу свойств выбранного** объекта. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ заполняет\]
</dt> <dd>

Адрес структуры [**\_ \_ данных сфвм**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .

</dd> </dl>

## <a name="remarks"></a>Примечания

Это сообщение играет по сути ту же функцию, что и [**ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Дополнительные сведения см. в статье [Создание обработчиков страницы свойств](propsheet-handlers.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
