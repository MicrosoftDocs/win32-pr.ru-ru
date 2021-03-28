---
description: Возвращает текущий монитор по умолчанию.
title: 'Метод Имултимонитордоккингсите::'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997839"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>Метод Имултимонитордоккингсите::

Возвращает текущий монитор по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пунксрк* \[ окне\]
</dt> <dd>

Тип: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Указатель на объект, реализующий интерфейс [_ *идоккингвиндов* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого запрашивается монитор.

</dd> <dt>

*фмон* \[ заполняет\]
</dt> <dd>

Тип: **хмонитор \** _

При возврате функции содержит указатель на обработчик монитора по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |



 

 
