---
description: Метод постановки \_ Alpha задает альфа-значение для всего изображения.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'Идксталфасеттер: метод ut_Alpha:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69d42bd73d0c716b7a5f3cdee413259340726538036a5dcd9cc7b5dcc8c8311a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998646"
---
# <a name="idxtalphasetterput_alpha-method"></a>Идксталфасеттер::p \_ методу UT Alpha

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Alpha`Метод задает альфа-значение для всего изображения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Альфа-канал* \[ окне\]
</dt> <dd>

Альфа-значение. Это значение будет применено ко всему целевому образу. Чтобы отключить это свойство, задайте отрицательное значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если для этого свойства задано неотрицательное значение, необходимо также отключить свойство alpha пандус, вызвав метод Set **\_ алфарамп** с отрицательным значением. В противном случае результат будет отображаться неправильно.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Идксталфасеттер**](idxtalphasetter.md)
</dt> <dt>

[**Идксталфасеттер::p UT \_ алфарамп**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 




