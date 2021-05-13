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
ms.openlocfilehash: 2cd437fd6c0e842eb314db6c57420af6b54b05ff
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840645"
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

Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Указатель на объект, реализующий интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого запрашивается монитор.

</dd> <dt>

*фмон* \[ заполняет\]
</dt> <dd>

Тип: **хмонитор \***

При возврате функции содержит указатель на обработчик монитора по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |



 

 
