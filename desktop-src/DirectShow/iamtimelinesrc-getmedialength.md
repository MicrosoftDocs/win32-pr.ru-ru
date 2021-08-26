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
ms.openlocfilehash: 72aeb68b3b3f9b31dc9ba00b2ffe8d82e2df8f8c5271abffcbd7737fa65203ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131184"
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



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[**Иамтимелинесрк:: Сетмедиаленгс**](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




