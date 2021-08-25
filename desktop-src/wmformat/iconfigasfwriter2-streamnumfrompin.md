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
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839825"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>Метод IConfigAsfWriter2:: Стреамнумфромпин

Метод **стреамнумфромпин** извлекает номер потока, связанный с указанным входным закреплением.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
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

## <a name="remarks"></a>Remarks

иногда может потребоваться использовать интерфейсы пакета SDK Windows Media Format напрямую для работы с потоком перед выполнением графа фильтра. так как вы не можете предположить, что номер потока ASF совпадает с DirectShow pin-кодом, предоставляется этот метод.

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 