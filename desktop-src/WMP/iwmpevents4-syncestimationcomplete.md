---
title: IWMPEvents4 Синцестиматионкомплете, метод
description: Событие Синцестиматионкомплете возникает при завершении оценки размера, ранее инициированной IWMPSyncDevice3 Естиматесинксизе.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Синцестиматионкомплете метод Windows Media Player
- Синцестиматионкомплете метод проигрывателя Windows Media Player, интерфейс IWMPEvents4
- Интерфейс IWMPEvents4 Windows Media Player, метод Синцестиматионкомплете
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788677"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a>Метод IWMPEvents4:: Синцестиматионкомплете

Событие **синцестиматионкомплете** возникает при завершении оценки размера, которая ранее была инициирована [**IWMPSyncDevice3:: естиматесинксизе**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize).

## <a name="syntax"></a>Синтаксис


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**ивмпсинкдевице**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) , представляющий устройство, для которого была инициирована оценка размера.

</dd> <dt>

*хрресулт* \[ окне\]
</dt> <dd>

Значение, указывающее на успешное или неуспешное выполнение оценки.



| Значение                                                                                                                                       | Значение                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_ОК**</dt> </dl>          | Оценка прошла удачно.<br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <dt>**\_прервать**</dt> </dl> | Оценка была прервана.<br/> |



 

</dd> <dt>

*лестиматедуседспаце* \[ окне\]
</dt> <dd>

Предполагаемое пространство (в байтах), которое будет использоваться на устройстве.

</dd> <dt>

*лестиматедсизе* \[ окне\]
</dt> <dd>

Предполагаемый размер (в байтах) синхронизируемых данных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[**IWMPSyncDevice3:: Естиматесинксизе**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





