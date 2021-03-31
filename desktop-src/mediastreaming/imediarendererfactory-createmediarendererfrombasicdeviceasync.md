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
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069905"
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



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имедиарендерерфактори**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

