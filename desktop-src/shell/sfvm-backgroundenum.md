---
description: 'Позволяет объекту обратного вызова запрашивать перечисление в фоновом потоке. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_BACKGROUNDENUM (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997827"
---
# <a name="sfvm_backgroundenum-message"></a>\_Сообщение сфвм баккграунденум

Позволяет объекту обратного вызова запрашивать перечисление в фоновом потоке. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Параметры

Это сообщение не содержит параметров.

## <a name="remarks"></a>Примечания

В ответ на это уведомление необходимо вернуть \_ значение ОК, чтобы включить перечисление фона. По умолчанию объект системной папки будет отображать анимацию "фонарик" во время перечисления. Чтобы задать пользовательскую анимацию, обработайте [**СФВМ \_ Animation**](sfvm-getanimation.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
