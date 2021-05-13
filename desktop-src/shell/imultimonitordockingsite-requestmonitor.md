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
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841975"
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

Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Указатель на объект, реализующий интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .

</dd> <dt>

*фмон* \[ окне\]
</dt> <dd>

Тип: **хмонитор \***

Указатель на обработчик монитора по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |



 

 
