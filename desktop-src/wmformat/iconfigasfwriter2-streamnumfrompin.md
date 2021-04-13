---
title: IConfigAsfWriter2 Стреамнумфромпин, метод
description: Метод Стреамнумфромпин извлекает номер потока, связанный с указанным входным закреплением.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Формат Windows Media, Стреамнумфромпин метод
- Стреамнумфромпин метод Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 Windows Media Format, метод Стреамнумфромпин
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413098"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>Метод IConfigAsfWriter2:: Стреамнумфромпин

Метод **стреамнумфромпин** извлекает номер потока, связанный с указанным входным закреплением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* \[ окне\]
</dt> <dd>

Указатель на интерфейс **Ипин** входного ПИН-кода.

</dd> <dt>

*пвстреамнум* \[ заполняет\]
</dt> <dd>

Указатель, получающий номер потока.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение S \_ ОК. В случае сбоя возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Иногда может потребоваться использовать интерфейсы пакета SDK Windows Media Format напрямую для работы с потоком перед выполнением графа фильтра. Поскольку нельзя предположить, что номер потока ASF совпадает с PIN-номером DirectShow, этот метод предоставляется.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 