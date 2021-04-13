---
title: IDWriteFactory2 Жетсистемфонтфаллбакк, метод
description: Создает резервный объект шрифта из списка резервных шрифтов системы.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Непосредственная запись метода Жетсистемфонтфаллбакк
- Прямая запись метода Жетсистемфонтфаллбакк, интерфейс IDWriteFactory2
- Прямая запись интерфейса IDWriteFactory2, метод Жетсистемфонтфаллбакк
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413409"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a>Метод IDWriteFactory2:: Жетсистемфонтфаллбакк

Создает резервный объект шрифта из списка резервных шрифтов системы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фонтфаллбакк* \[ заполняет\]
</dt> <dd>

Тип: **[ **идвритефонтфаллбакк**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***

Содержит адрес указателя на вновь созданный объект резервного шрифта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

 