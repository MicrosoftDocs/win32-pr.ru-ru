---
description: Возвращает идентификатор интерфейса гибкой ссылки на объект.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Метод Иагилереференце:: Resolve'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 0b58013ba81bb394715a0042f3f3d7435a381fa01f5b985bd9ad81d12122441e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758783"
---
# <a name="iagilereferenceresolve-method"></a>Метод Иагилереференце:: Resolve

Возвращает идентификатор интерфейса гибкой ссылки на объект.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*riid* \[ окне\]
</dt> <dd>

Идентификатор интерфейса для извлечения из ссылки Agile. Он не обязательно должен совпадать с зарегистрированным интерфейсом.

</dd> <dt>

*ппвобжектреференце* \[ out, retval\]
</dt> <dd>

При успешном завершении \* *ппвобжектреференце* является указателем на интерфейс, заданный параметром *riid*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Возвращаемое значение                                                                              | Описание                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>\_ОК</dt> </dl>          | Метод завершился успешно.<br/>                                  |
| <dl> <dt>\_интерфейс E</dt> </dl> | Запрошенный интерфейс не реализован в зарегистрированном объекте.<br/> |



 

## <a name="remarks"></a>Remarks

Вызовите функцию [**рожетагилереференце**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) , чтобы создать динамическую ссылку на объект. Вызовите метод **Resolve** для локализации объекта в апартамент, в котором вызывается **разрешение Resolve** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>            |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иагилереференце**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**рожетагилереференце**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




