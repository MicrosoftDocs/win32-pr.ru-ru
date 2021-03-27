---
description: 'Позволяет объекту обратного вызова указывать файл справки HTML и раздел внутри него. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETHELPTOPIC (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911396"
---
# <a name="sfvm_gethelptopic-message"></a>\_Сообщение сфвм жеселптопик

Позволяет объекту обратного вызова указывать файл справки HTML и раздел внутри него. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ФТД* \[ заполняет\]
</dt> <dd>

Адрес структуры [**\_ \_ данных сфвм хелптопик**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) , которая указывает файл справки HTML и раздел.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
