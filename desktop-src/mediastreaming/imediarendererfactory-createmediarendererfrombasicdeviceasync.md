---
title: Имедиарендерерфактори Креатемедиарендерерфромбасикдевицеасинк, метод
description: Асинхронно создает новый экземпляр объекта, который реализует интерфейс Имедиарендерер, используя указанный интерфейс Ибасикдевице.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API потоковой передачи мультимедиа метода Креатемедиарендерерфромбасикдевицеасинк
- API потоковой передачи мультимедиа метода Креатемедиарендерерфромбасикдевицеасинк, интерфейс Имедиарендерерфактори
- API потоковой передачи мультимедиа интерфейса Имедиарендерерфактори, метод Креатемедиарендерерфромбасикдевицеасинк
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b9ee80a4f681bb57d62f84d35cf3a254e38982a10f642a35e35187f6af9e48e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092294"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a>Метод Имедиарендерерфактори:: Креатемедиарендерерфромбасикдевицеасинк

Асинхронно создает новый экземпляр объекта, который реализует интерфейс [**имедиарендерер**](imediarenderer.md) , используя указанный интерфейс [**ибасикдевице**](ibasicdevice.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*басикдевице* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**ибасикдевице**](ibasicdevice.md) , представляющий устройство, для которого будет создан экземпляр [**имедиарендерер**](imediarenderer.md) .

</dd> <dt>

*значение* \[ out, retval\]
</dt> <dd>

Получает ссылку на объект [**креатемедиарендерероператион**](createmediarendereroperation.md) , используемый для получения результатов асинхронной операции.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**имедиарендерерфактори**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

