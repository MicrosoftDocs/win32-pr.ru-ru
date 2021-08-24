---
description: Метод Get \_ BorderColor извлекает цвет границы вокруг границ шаблона очистки.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: 'Метод Идкстжпег:: get_BorderColor (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3769a5d5e790f03343c4978b1397c8e14e0d32f316870ec3e4a6d2c449a54d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341344"
---
# <a name="idxtjpegget_bordercolor-method"></a>Метод Идкстжпег:: Get \_ BorderColor

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_BorderColor`Метод получает цвет границы вокруг границ шаблона очистки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает цвет. Возвращаемое значение представляет собой шестнадцатеричное число в формате 0xRRGGBB, где RR — это значение красного цвета, а параметр GG — зеленое значение, а BB — синий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Идкстжпег**](idxtjpeg.md)
</dt> </dl>

 

 




