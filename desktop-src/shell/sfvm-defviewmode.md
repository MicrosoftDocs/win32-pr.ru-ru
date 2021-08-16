---
description: 'Позволяет объекту обратного вызова указать режим представления. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_DEFVIEWMODE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 28958fd992f70924ebbd51c06090d3a55c0ef8e6418d1ee055c5eb534acb9d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090164"
---
# <a name="sfvm_defviewmode-message"></a>\_Сообщение сфвм дефвиевмоде

Позволяет объекту обратного вызова указать режим представления. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиевмоде* \[ заполняет\]
</dt> <dd>

Одно из значений перечисляемого типа [**фолдервиевмоде**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
