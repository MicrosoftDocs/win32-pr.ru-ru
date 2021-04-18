---
description: Метод Сетрекомпформатфромсаурце задает формат повторного сжатия видео, используя формат сжатия из исходного файла.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Метод Иамтимелинеграуп:: Сетрекомпформатфромсаурце (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679734"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>Метод Иамтимелинеграуп:: Сетрекомпформатфромсаурце

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetRecompFormatFromSource`Метод задает формат повторного сжатия видео, используя формат сжатия из исходного файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псаурце* 
</dt> <dd>

Указатель на интерфейс [**иамтимелинесрк**](iamtimelinesrc.md) исходного объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значения **HRESULT** . Ниже приведены возможные значения.



| Код возврата                                                                                             | Описание                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                    | Успешно.<br/>                                                                                    |
| <dl> <dt>**\_нет \_ временной шкалы**</dt> </dl>          | Группа находится за пределами временной шкалы.<br/>                                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Недостаточно памяти.<br/>                                                                        |
| <dl> <dt>**\_указатель E**</dt> </dl>               | **Пустой** аргумент указателя.<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ инвалидмедиатипе**</dt> </dl> | Недопустимый тип носителя. Группа не является видеогруппой, или исходный файл не имеет потока видео.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод находит исходный файл, связанный с *псаурце*, Извлекает тип носителя первого видеопотока в файле и задает формат сжатия группы с помощью этого типа. Дополнительные сведения о форматах сжатия см. в разделе [**иамтимелинеграуп:: сетсмартрекомпрессформат**](iamtimelinegroup-setsmartrecompressformat.md).

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

[**Интерфейс Иамтимелинеграуп**](iamtimelinegroup.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




