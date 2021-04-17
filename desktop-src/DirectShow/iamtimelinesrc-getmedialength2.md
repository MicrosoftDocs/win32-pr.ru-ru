---
description: 'Метод GetMediaLength2 извлекает длину носителя этого исходного объекта. Этот метод эквивалентен Иамтимелинесрк:: Жетмедиаленгс, но принимает значения РЕФТИМЕ.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Метод Иамтимелинесрк:: GetMediaLength2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685080"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a>Метод Иамтимелинесрк:: GetMediaLength2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetMediaLength2`Метод получает длину носителя этого исходного объекта. Этот метод эквивалентен [**иамтимелинесрк:: жетмедиаленгс**](iamtimelinesrc-getmedialength.md), но принимает значения [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пленгс* 
</dt> <dd>

Получает длину носителя в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                     | Описание                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>            | Успешно.<br/>                                |
| <dl> <dt>**E \_ нотдетерминед**</dt> </dl> | Для этого объекта не заданы значения времени носителя.<br/> |
| <dl> <dt>**\_указатель E**</dt> </dl>       | **Пустой** аргумент указателя.<br/>              |



 

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

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




