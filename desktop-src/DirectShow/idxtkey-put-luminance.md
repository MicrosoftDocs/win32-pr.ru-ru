---
description: Метод «разместить \_ светимость» указывает значение светимости, к которому будет подключаться ключ. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ светимость.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: 'Идксткэй: метод ut_Luminance:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae51fe72220355cb6e206ea437f547a0a8ca2d77633195debeb364f17e7f136f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819387"
---
# <a name="idxtkeyput_luminance-method"></a>Идксткэй: \_ метод освещенности:p UT

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Luminance`Метод задает значение светимости для ключа. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ светимость.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Значение светимости, на которое следует подключаться. Допустимый диапазон: от 0 до 100.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Идксткэй**](idxtkey.md)
</dt> <dt>

[**Идксткэй::p UT \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




