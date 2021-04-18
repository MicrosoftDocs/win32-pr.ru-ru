---
description: Метод Жетконнектедмедиатипе Извлекает тип носителя для соединения по входному закрепления образца захвата.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Метод Исамплеграббер:: Жетконнектедмедиатипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674972"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>Метод Исамплеграббер:: Жетконнектедмедиатипе

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetConnectedMediaType`Метод извлекает тип носителя для соединения по входному закрепления образца захвата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птипе* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , выделенную вызывающей стороной.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                                           | Описание                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_указатель E**</dt> </dl>             | **Пустой** аргумент указателя.<br/>   |
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>                     |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | Фильтр не подключен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод копирует тип носителя в структуру **AM \_ Media \_ Type** , заданную параметром *птипе*. Вызывающий объект должен освободить блок формата типа мультимедиа. Можно использовать функцию **CoTaskMemFree** или функцию [**фримедиатипе**](freemediatype.md) в библиотеке базового класса.

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

[Использование образца захвата](using-the-sample-grabber.md)
</dt> <dt>

[**Интерфейс Исамплеграббер**](isamplegrabber.md)
</dt> </dl>

 

 




