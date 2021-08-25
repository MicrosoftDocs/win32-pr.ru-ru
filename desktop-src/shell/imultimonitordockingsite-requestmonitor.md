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
ms.openlocfilehash: 9e5eeb2b99455d81bae36f1c5f26ed38126122bb58a5b8964a47cfb205f71ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942904"
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
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                   |



 

 
