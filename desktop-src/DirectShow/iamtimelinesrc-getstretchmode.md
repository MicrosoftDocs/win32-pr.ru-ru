---
description: Метод Жетстретчмоде извлекает режим Stretch. Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.
ms.assetid: d9a3d283-edb5-40be-b877-69cb23462afa
title: 'Метод Иамтимелинесрк:: Жетстретчмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 53be58df0315c4a03c62369f746efa510c2024fa030c3bef75eb4ff08505b1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952913"
---
# <a name="iamtimelinesrcgetstretchmode-method"></a>Метод Иамтимелинесрк:: Жетстретчмоде

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetStretchMode`Метод извлекает режим растяжения. Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStretchMode(
   int *pnStretchMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнстретчмоде* 
</dt> <dd>

Получает флаг, указывающий текущий режим Stretch. Список возможных значений см. в разделе [**изменение размера флагов**](resize-flags.md).

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

[**Интерфейс Иамтимелинесрк**](iamtimelinesrc.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




