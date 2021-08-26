---
description: Метод Get \_ Alpha извлекает альфа-значение для всего изображения.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Метод Идксталфасеттер:: get_Alpha (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 054e2a1745f96dc4d6ea846bed0448948fae8407dd6ab44d2796742e405f2e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051974"
---
# <a name="idxtalphasetterget_alpha-method"></a>Метод Идксталфасеттер:: Get \_ Alpha

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_Alpha`Метод получает альфа-значение для всего изображения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*палфа* \[ out, retval\]
</dt> <dd>

Получает альфа-значение. Это альфа-значение будет применено ко всему целевому образу. Отрицательное значение указывает, что альфа-значение не задано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                               | Описание                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>      | Success<br/>                   |



 

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

[**Интерфейс Идксталфасеттер**](idxtalphasetter.md)
</dt> </dl>

 

 




