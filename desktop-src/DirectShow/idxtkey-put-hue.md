---
description: Метод «разместить \_ оттенок» задает значение оттенка, по которому будет указывать ключ. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙный \_ тон.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'Идксткэй: метод ut_Hue:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675321"
---
# <a name="idxtkeyput_hue-method"></a>Идксткэй::p \_ метод оттенок метода UT

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Hue`Метод задает значение оттенка ключа. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙный \_ тон.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Значение оттенка ключа. Допустимый диапазон: от 0 до 360.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Идксткэй**](idxtkey.md)
</dt> <dt>

[**Идксткэй::p UT \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




