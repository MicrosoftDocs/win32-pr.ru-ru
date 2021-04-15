---
description: Метод Жетмедиаленгс извлекает длину носителя этого исходного объекта.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'Метод Иамтимелинесрк:: Жетмедиаленгс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675732"
---
# <a name="iamtimelinesrcgetmedialength-method"></a>Метод Иамтимелинесрк:: Жетмедиаленгс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetMediaLength`Метод получает длину носителя этого исходного объекта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пленгс* 
</dt> <dd>

Получает длину носителя в 100-наносекундных единицах.

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

[**Иамтимелинесрк:: Сетмедиаленгс**](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




