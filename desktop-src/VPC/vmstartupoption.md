---
title: Перечисление Вмстартупоптион (Впккоминтерфацес. h)
description: Указывает параметр запуска.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- Перечисление Вмстартупоптион Virtual PC
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9799f4eb797c76be9c37b458551f99e0067977f42422c4b4181cee66c92527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998464"
---
# <a name="vmstartupoption-enumeration"></a>Перечисление Вмстартупоптион

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Указывает параметр запуска.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**Вмстартупоптион, \_ Обычная**
</dt> <dd>

Запуск в обычном режиме.

</dd> <dt>

<span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**Вмстартупоптион \_ фикспаренттиместампмисматч**
</dt> <dd>

Исправьте несоответствие родительской метки времени.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ивмвиртуалмачине:: Startup2**](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

