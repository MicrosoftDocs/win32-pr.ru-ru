---
description: 'Позволяет объекту обратного вызова указать текст справки для пунктов меню или кнопок панели инструментов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETHELPTEXT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c015c1999cbd60174da1994d92766b4f334630294767ee390be21340aef97cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661024"
---
# <a name="sfvm_gethelptext-message"></a>\_Сообщение сфвм жеселптекст

Позволяет объекту обратного вызова указать текст справки для пунктов меню или кнопок панели инструментов. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идкмд \_ кчмакс* \[ в\]
</dt> <dd>

Слово с низким приоритетом для этого параметра содержит идентификатор команды. Слово в высоком порядке содержит количество символов в буфере *псзтекст* .

</dd> <dt>

*псзтекст* \[ заполняет\]
</dt> <dd>

Строка, заканчивающаяся нулем и содержащая текст справки.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
