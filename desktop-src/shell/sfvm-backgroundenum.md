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
ms.openlocfilehash: 724f971f52b57a008ec17ac316b78839a6890e3e2efee5d5a037ab4fdcd7ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592744"
---
# <a name="sfvm_backgroundenum-message"></a>\_Сообщение сфвм баккграунденум

Позволяет объекту обратного вызова запрашивать перечисление в фоновом потоке. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Параметры

Это сообщение не содержит параметров.

## <a name="remarks"></a>Remarks

В ответ на это уведомление необходимо вернуть \_ значение ОК, чтобы включить перечисление фона. По умолчанию объект системной папки будет отображать анимацию "фонарик" во время перечисления. Чтобы задать пользовательскую анимацию, обработайте [**СФВМ \_ Animation**](sfvm-getanimation.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
