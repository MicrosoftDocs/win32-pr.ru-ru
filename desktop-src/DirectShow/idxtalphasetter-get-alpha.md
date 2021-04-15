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
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688802"
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
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно<br/>                   |



 

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

[**Интерфейс Идксталфасеттер**](idxtalphasetter.md)
</dt> </dl>

 

 




