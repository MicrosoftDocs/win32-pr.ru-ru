---
description: 'позволяет объекту обратного вызова объединять пункты меню в меню обозревателя Windows. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
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
ms.openlocfilehash: 5f6838b3c2ee845794bfa506beada2b7092f1bb918438f820f0e77d6b6543dc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111174"
---
# <a name="sfvm_mergemenu-message"></a>\_Сообщение сфвм мержемену

позволяет объекту обратного вызова объединять пункты меню в меню обозревателя Windows. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


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

## <a name="remarks"></a>Remarks

Это сообщение, по сути, такое же самое, что и [**ишеллбровсер:: инсертменуссб**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) и [**Ишеллбровсер:: сетменусб**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) в представлении пользовательской папки. см. раздел *использование ишеллбровсер для взаимодействия с обозревателем Windows в* разделе [реализация представления папки](../lwef/nse-folderview.md) для дальнейшего обсуждения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
