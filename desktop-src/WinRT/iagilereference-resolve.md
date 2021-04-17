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
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701575"
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



 

## <a name="remarks"></a>Комментарии

Вызовите функцию [**рожетагилереференце**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) , чтобы создать динамическую ссылку на объект. Вызовите метод **Resolve** для локализации объекта в апартамент, в котором вызывается **разрешение Resolve** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>            |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иагилереференце**](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[**рожетагилереференце**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




