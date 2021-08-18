---
title: Структура MPCOMPONENT_STATUS (Мпклиент. h)
description: Сведения о состоянии компонента.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- MPCOMPONENT_STATUS структуры устаревшие функции среды Windows
- функции PMPCOMPONENT_STATUS Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747802"
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
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





