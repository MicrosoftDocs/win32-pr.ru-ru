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
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997967"
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

Тип: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Указатель на объект, реализующий интерфейс [_ *идоккингвиндов* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) , для которого изменяется монитор.

</dd> <dt>

*хмоннев* \[ окне\]
</dt> <dd>

Тип: **хмонитор**

Маркер монитора, который заменяет существующий монитор по умолчанию.

</dd> <dt>

*фмонолд* \[ заполняет\]
</dt> <dd>

Тип: **хмонитор \** _

При возврате этой функции содержит указатель на предыдущий обработчик монитора по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/> |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                   |



 

 
