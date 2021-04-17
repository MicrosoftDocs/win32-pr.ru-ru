---
description: Возвращает номер версии системы событий.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: 'Метод IEventSystem2:: метода Version'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2c75538d9fd71cb8ee81e454249fd5116ccd090c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496656"
---
# <a name="ieventsystem2getversion-method"></a>Метод IEventSystem2:: метода Version

Возвращает номер версии системы событий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнверсион* \[ заполняет\]
</dt> <dd>

Номер версии системы событий.

</dd> </dl>

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

 

 




