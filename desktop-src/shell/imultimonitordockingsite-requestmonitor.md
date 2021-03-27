---
description: Проверяет, что монитор активен и доступен.
title: 'Метод Имултимонитордоккингсите:: Рекуестмонитор'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999705"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>Метод Имултимонитордоккингсите:: Рекуестмонитор

Проверяет, что монитор активен и доступен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пунксрк* \[ окне\]
</dt> <dd>

Тип: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Указатель на объект, реализующий интерфейс [_ *идоккингвиндов* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .

</dd> <dt>

*фмон* \[ окне\]
</dt> <dd>

Тип: **хмонитор \** _

Указатель на обработчик монитора по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |



 

 
