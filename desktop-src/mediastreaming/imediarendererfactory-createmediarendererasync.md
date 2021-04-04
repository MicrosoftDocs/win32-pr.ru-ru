---
title: Имедиарендерерфактори Креатемедиарендерерасинк, метод
description: Асинхронно создает новый экземпляр объекта, который реализует интерфейс Имедиарендерер, используя указанное уникальное имя устройства (УДН).
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API потоковой передачи мультимедиа метода Креатемедиарендерерасинк
- API потоковой передачи мультимедиа метода Креатемедиарендерерасинк, интерфейс Имедиарендерерфактори
- API потоковой передачи мультимедиа интерфейса Имедиарендерерфактори, метод Креатемедиарендерерасинк
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790561"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a>Метод Имедиарендерерфактори:: Креатемедиарендерерасинк

Асинхронно создает новый экземпляр объекта, который реализует интерфейс [**имедиарендерер**](imediarenderer.md) , используя указанное уникальное имя устройства (УДН).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*девицеидентифиер* \[ окне\]
</dt> <dd>

Объект HSTRING, содержащий УДН, который идентифицирует устройство DLNA ДМР, для которого будет создан экземпляр [**имедиарендерер**](imediarenderer.md) .

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

 

