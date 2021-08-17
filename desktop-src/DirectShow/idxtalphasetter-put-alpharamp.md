---
description: Метод размещения \_ алфарамп задает свойство alpha пандус. Альфа-шкала — это процентная доля, на которую корректируются значения альфа в исходном изображении. Например, если альфа-пандус имеет значение 0,5, то значения альфа в изображении уменьшаются на 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'Идксталфасеттер: метод ut_AlphaRamp:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88661c40ea0824d643909f688a7d86251c434e0e3dcc88d8a3aec97dcb6b40c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952733"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>Идксталфасеттер::p UT \_ алфарамп метод

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_AlphaRamp`Метод задает свойство alpha пандус. Альфа-шкала — это процентная доля, на которую корректируются значения альфа в исходном изображении. Например, если альфа-пандус имеет значение 0,5, то значения альфа в изображении уменьшаются на 50%.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Альфа-канал* \[ окне\]
</dt> <dd>

Альфа-шкала в процентах. Например, 1,0 — 100%. Чтобы отключить это свойство, задайте отрицательное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если для этого свойства задано неотрицательное значение, необходимо также отключить свойство Alpha, вызвав метод Set **\_ Alpha** с отрицательным значением. В противном случае результат будет отображаться неправильно.

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

[**Интерфейс Идксталфасеттер**](idxtalphasetter.md)
</dt> <dt>

[**Идксталфасеттер::p UT \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




