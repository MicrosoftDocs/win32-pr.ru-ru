---
description: Метод Жетнексттранс извлекает первый переход, который отображается в указанное время или позже.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Метод Иамтимелинетрансабле:: Жетнексттранс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685047"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>Метод Иамтимелинетрансабле:: Жетнексттранс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetNextTrans`Метод извлекает первый переход, который отображается в указанное время или позже.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пптранс* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) объекта перехода.

</dd> <dt>

*\Sub* 
</dt> <dd>

Указатель на переменную, указывающую время в 100-наносекундных единицах. В поле входное значение указывает время, с которого нужно найти переход. В выходных данных, если переход получен, это значение устанавливается равным времени окончания перехода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ ОК, если метод получает переход, или \_ значение false, если не удается найти переход. В противном случае возвращает значение **HRESULT** , указывающее причину сбоя.

## <a name="remarks"></a>Комментарии

Время начала перехода может быть меньше времени, указанного в *схеме контактов*, если переход охватывает указанное время.

Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс [**иамтимелинеобж**](iamtimelineobj.md) имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

[**Интерфейс Иамтимелинетрансабле**](iamtimelinetransable.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




