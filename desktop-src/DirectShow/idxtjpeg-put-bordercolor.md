---
description: Метод «разместить \_ BorderColor» задает цвет границы вокруг краев шаблона очистки.
ms.assetid: d6a49956-8fc9-4ba2-8485-a49175da3cf7
title: 'Идкстжпег: метод ut_BorderColor:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faacc76eaa120467aa6cfb6c318aac0d9baec334
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675116"
---
# <a name="idxtjpegput_bordercolor-method"></a>Идкстжпег::p \_ методу UT BorderColor

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_BorderColor`Метод задает цвет границы вокруг границ шаблона очистки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_BorderColor(
  [in] long newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Задает цвет в виде шестнадцатеричного числа в формате 0xRRGGBB, где RR — это красная величина, а параметр GG — зеленое значение, а BB — синий.

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

[**Интерфейс Идкстжпег**](idxtjpeg.md)
</dt> </dl>

 

 




