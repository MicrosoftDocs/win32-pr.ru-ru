---
title: IWMPEvents4 Синцестиматионкомплете, метод
description: Событие Синцестиматионкомплете возникает при завершении оценки размера, ранее инициированной IWMPSyncDevice3 Естиматесинксизе.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- проигрыватель Windows Media метода синцестиматионкомплете
- проигрыватель Windows Media метода синцестиматионкомплете, интерфейс IWMPEvents4
- проигрыватель Windows Media интерфейса IWMPEvents4, метод синцестиматионкомплете
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3f444cdc66874c907bb4c6412fa10384fde67145563d79153c28cb675c6fc3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575609"
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

 

 





