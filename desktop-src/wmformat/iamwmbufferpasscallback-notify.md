---
title: Метод уведомления Иамвмбуфферпасскаллбакк
description: Метод notify вызывается ПИН-кодом для каждого буфера, который доставляется во время потоковой передачи.
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
keywords:
- Уведомлять о методе Windows Media Format
- Уведомлять о методе Windows Media Format, интерфейс Иамвмбуфферпасскаллбакк
- Интерфейс Иамвмбуфферпасскаллбакк Windows Media Format, метод notify
topic_type:
- apiref
api_name:
- IAMWMBufferPassCallback.Notify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f364243e40400884287c6219698991ccf8afc0be86a85ec612a5b193253994dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847539"
---
# <a name="iamwmbufferpasscallbacknotify-method"></a>Метод Иамвмбуфферпасскаллбакк:: notify

Метод **Notify** вызывается ПИН-кодом для каждого буфера, который доставляется во время потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Notify(
  [in] INSSBuffer3    *pNSSBuffer3,
  [in] IPin           *pPin,
  [in] REFERENCE_TIME *prtStart,
  [in] REFERENCE_TIME *prtEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pNSSBuffer3* \[ окне\]
</dt> <dd>

Указатель на интерфейс [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) , предоставленный в примере носителя.

</dd> <dt>

*ппин* \[ окне\]
</dt> <dd>

Указатель на ПИН-код, связанный с потоком мультимедиа, к которому принадлежит образец.

</dd> <dt>

*пртстарт* \[ окне\]
</dt> <dd>

Время начала примера.

</dd> <dt>

*пртенд* \[ окне\]
</dt> <dd>

Время окончания примера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Не указано конкретное возвращаемое значение. Вызывающий ПИН-код игнорирует значение **HRESULT**.

## <a name="remarks"></a>Remarks

Этот метод позволяет приложению проверять данные в буфере мультимедиа перед обработкой содержимого буфера и работать с ними. Приложение несет ответственность за знание типа носителя в ПИН-коде. Эти сведения можно получить, сначала получив сведения о потоке из профиля, а затем вызвав метод [**IConfigAsfWriter2:: стреамнумфромпин**](iconfigasfwriter2-streamnumfrompin.md) , чтобы определить, какой ПИН-код связан с каждым потоком.

## <a name="see-also"></a>См. также

<dl> <dt>

[**DirectShow Справочник по КАСФ**](directshow-qasf-reference.md)
</dt> <dt>

[**Интерфейс Иамвмбуфферпасскаллбакк**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback)
</dt> <dt>

[**Интерфейс INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)
</dt> </dl>

 

 