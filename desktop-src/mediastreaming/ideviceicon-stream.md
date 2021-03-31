---
title: Идевицеикон Stream, метод
description: Получает значок в виде потока.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Потоковый интерфейс API потоковой передачи мультимедиа
- API потокового метода потокового мультимедиа, интерфейс Идевицеикон
- API потоковой передачи мультимедиа интерфейса Идевицеикон, потоковый метод
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337409"
---
# <a name="ideviceiconstream-method"></a>Метод Идевицеикон:: Stream

Получает значок в виде потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*значение* \[ заполняет\]
</dt> <dd>

Получает ссылку на объект [**ирандомакцессстреамвисконтенттипе**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) , который можно использовать для получения данных изображения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идевицеикон**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

