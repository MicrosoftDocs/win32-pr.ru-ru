---
title: Бесплатный метод Имеморяллокатор
description: Метод Free освобождает память, выделенную методом выделения.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- структурированный служба хранилища метода Free
- структурированный метод служба хранилища, интерфейс имеморяллокатор
- структурированный служба хранилища интерфейса имеморяллокатор, бесплатный метод
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78690a37b5500f5e540cf4c2ef516b7c3ea89c219ba475dc5e5ac030f775d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906174"
---
# <a name="imemoryallocatorfree-method"></a>Метод Имеморяллокатор:: Free

Метод **Free** освобождает память, выделенную методом [**выделения**](imemoryallocator-allocate.md) .

## <a name="syntax"></a>Синтаксис


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PV* 
</dt> <dd>

Указатель на память, которую необходимо освободить.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Библиотека<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 





