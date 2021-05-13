---
description: Изменения, которые монитор используется для закрепленных панелей инструментов в системе с несколькими мониторами.
title: 'Метод Имултимонитордоккингсите:: Сетмонитор'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841945"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>Метод Имултимонитордоккингсите:: Сетмонитор

Изменения, которые монитор используется для закрепленных панелей инструментов в системе с несколькими мониторами.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пунксрк* \[ окне\]
</dt> <dd>

Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Указатель на объект, реализующий интерфейс [**идоккингвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого изменяется монитор.

</dd> <dt>

*хмоннев* \[ окне\]
</dt> <dd>

Тип: **хмонитор**

Маркер монитора, который заменяет существующий монитор по умолчанию.

</dd> <dt>

*фмонолд* \[ заполняет\]
</dt> <dd>

Тип: **хмонитор \***

При возврате этой функции содержит указатель на предыдущий обработчик монитора по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |



 

 
