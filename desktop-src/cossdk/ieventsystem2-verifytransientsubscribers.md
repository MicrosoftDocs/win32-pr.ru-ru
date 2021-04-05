---
description: Проверяет существование всех временных подписчиков в хранилище данных. Вызывая этот метод, можно убедиться, что все временные подписчики, перечисленные в хранилище данных, активны.
ms.assetid: fffdde33-e960-42ef-a089-8ea8a6f33d52
title: 'Метод IEventSystem2:: Верифитрансиентсубскриберс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.VerifyTransientSubscribers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4415f405b95f341b645ca1dccbf254df2ffc7167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990507"
---
# <a name="ieventsystem2verifytransientsubscribers-method"></a>Метод IEventSystem2:: Верифитрансиентсубскриберс

Проверяет существование всех временных подписчиков в хранилище данных. Вызывая этот метод, можно убедиться, что все временные подписчики, перечисленные в хранилище данных, активны.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT VerifyTransientSubscribers();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные, e \_ Fail и S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




