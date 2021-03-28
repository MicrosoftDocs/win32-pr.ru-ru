---
description: 'Позволяет объекту обратного вызова объединять пункты меню в меню проводника Windows. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_MERGEMENU (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986076"
---
# <a name="sfvm_mergemenu-message"></a>\_Сообщение сфвм мержемену

Позволяет объекту обратного вызова объединять пункты меню в меню проводника Windows. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинфо* \[ заполняет\]
</dt> <dd>

Структура [**ккминфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) , содержащая сведения, необходимые для слияния элементов в меню.

</dd> </dl>

## <a name="remarks"></a>Примечания

Это сообщение, по сути, такое же самое, что и [**ишеллбровсер:: инсертменуссб**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) и [**Ишеллбровсер:: сетменусб**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) в представлении пользовательской папки. Дополнительные сведения см. в разделе *Использование ишеллбровсер для взаимодействия с проводником Windows* в статье [Реализация представления папки](../lwef/nse-folderview.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
