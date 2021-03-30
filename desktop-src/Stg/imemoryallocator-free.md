---
title: Бесплатный метод Имеморяллокатор
description: Метод Free освобождает память, выделенную методом выделения.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Структурированное хранилище методов Free
- Структурированное хранилище методов Free, интерфейс Имеморяллокатор
- Имеморяллокатор интерфейс структурированного хранилища, Бесплатный метод
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
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071222"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Библиотека<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 





