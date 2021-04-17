---
description: Представляет тип сведений в \_ \_ структуре сведений о наборе ЦП системы \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Перечисление CPU_SET_INFORMATION_TYPE (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673773"
---
# <a name="cpu_set_information_type-enumeration"></a>\_ \_ Перечисление типов сведений о НАБОРе ЦП \_

Представляет тип сведений в структуре [**\_ \_ \_ сведений о наборе ЦП системы**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**кпусетинформатион**
</dt> <dd>

Структура содержит сведения о наборе ЦП.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                              |
| Header<br/>                   | <dl> <dt>Процесссреадсапи. h (включение Windows. h)</dt> </dl> |



 

 




