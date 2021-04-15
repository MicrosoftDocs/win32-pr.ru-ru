---
description: Метод Сетмедиаленгс задает длительность исходного файла.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'Метод Иамтимелинесрк:: Сетмедиаленгс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689359"
---
# <a name="iamtimelinesrcsetmedialength-method"></a>Метод Иамтимелинесрк:: Сетмедиаленгс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetMediaLength`Метод задает длительность исходного файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Длина* 
</dt> <dd>

Длина носителя (в 100-наносекундных единицах).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Можно избежать потенциальных ошибок отрисовки, установив длину носителя до того, как будет задано время окончания носителя. При задании времени окончания передачи данных DES проверяет его на соответствие длине носителя.

Этот метод не проверяет параметр *длины* , но значение должно равняться фактической длительности исходного файла. Получите длительность исходного файла, вызвав [**имедиадет:: Get \_ стреамленгс**](imediadet-get-streamlength.md).

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

 

 




