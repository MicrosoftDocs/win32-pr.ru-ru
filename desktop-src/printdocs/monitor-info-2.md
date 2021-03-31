---
description: В структуре MONITORing \_ \_ 2 определяется монитор.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Структура MONITOR_INFO_2 (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817897"
---
# <a name="monitor_info_2-structure"></a>\_Структура мониторинга информации \_ 2

В структуре **Monitoring \_ \_ 2** определяется монитор.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>Члены

<dl> <dt>

**pName**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая является именем монитора.

</dd> <dt>

**пенвиронмент**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая указывает среду, для которой был записан монитор (например, Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**пдллнаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая является именем библиотеки DLL монитора.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Винспул. h (включение Windows. h)</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **\_ \_ Сведения о \_ мониторинге 2W** (Юникод) и **\_ \_ сведения об мониторе \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Вывод на печать](printdocs-printing.md)
</dt> <dt>

[Структуры API диспетчера очереди печати](printing-and-print-spooler-structures.md)
</dt> <dt>

[**аддмонитор**](addmonitor.md)
</dt> <dt>

[**енуммониторс**](enummonitors.md)
</dt> <dt>

[**\_Сведения о мониторе \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




