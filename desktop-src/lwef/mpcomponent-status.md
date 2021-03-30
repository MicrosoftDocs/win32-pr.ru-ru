---
title: Структура MPCOMPONENT_STATUS (Мпклиент. h)
description: Сведения о состоянии компонента.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS структуры устаревшие функции среды Windows
- Функции PMPCOMPONENT_STATUS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801918"
---
# <a name="mpcomponent_status-structure"></a>\_Структура состояния мпкомпонент

Сведения о состоянии компонента.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Члены

<dl> <dt>

**фенабле**
</dt> <dd>

Тип: **bool** .

</dd> <dd>

Состояние компонента.

</dd> <dt>

**Состав**
</dt> <dd>

Тип: **HRESULT**

</dd> <dd>

Код успешного выполнения или ошибки, связанный с состоянием.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





