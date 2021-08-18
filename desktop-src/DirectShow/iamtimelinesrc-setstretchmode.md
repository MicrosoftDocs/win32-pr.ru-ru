---
description: Метод Сетстретчмоде задает режим Stretch. Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Метод Иамтимелинесрк:: Сетстретчмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c12d14edf665bb3257b627a194923c267ee9e8bd25027e40a7a975a15c10025f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148547"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>Метод Иамтимелинесрк:: Сетстретчмоде

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetStretchMode`Метод задает режим Stretch. Режим растяжения определяет способ подготовки источника видео, если его размер не соответствует выходным измерениям.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нстретчмоде* 
</dt> <dd>

Флаг, указывающий текущий режим Stretch. Список возможных значений см. в разделе [**изменение размера флагов**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

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

 

 




