---
description: Метод Ентербитмапграбмоде переключает средство обнаружения мультимедиа в режим захвата точечного рисунка и выполняет поиск графа фильтра в указанное время.
ms.assetid: 9351ce73-766c-4863-88a5-f974ede79ee6
title: 'Метод Имедиадет:: Ентербитмапграбмоде (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.EnterBitmapGrabMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d47989b95663a9a99f4363fb505aec996ea23acdd813cf301f7ee252c874dc78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952623"
---
# <a name="imediadetenterbitmapgrabmode-method"></a>Метод Имедиадет:: Ентербитмапграбмоде

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`EnterBitmapGrabMode`Метод переключает средство обнаружения мультимедиа в режим захвата точечного рисунка и выполняет поиск графа фильтра в указанное время.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnterBitmapGrabMode(
   double StreamTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стреамтиме* 
</dt> <dd>

Время в секундах, в течение которого граф ищет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения:



| Код возврата                                                                                             | Описание                                              |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                    | Успешно.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Недопустимый аргумент.<br/>                             |
| <dl> <dt>**VFW \_ E \_ инвалидмедиатипе**</dt> </dl> | Исходный файл не содержит поток видео.<br/> |
| <dl> <dt>**присвоено \_ \_ время действия VFW E \_**</dt> </dl>    | Время ожидания команды поиска истекло.<br/>                       |



 

## <a name="remarks"></a>Remarks

Перед вызовом этого метода задайте имя файла и поток, вызвав [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) и [**имедиадет::p UT \_ куррентстреам**](imediadet-put-currentstream.md).

Этот метод вставляет [**образец фильтра захвата**](sample-grabber-filter.md) в граф фильтра. Затем можно вызвать метод [**имедиадет:: жетсамплеграббер**](imediadet-getsamplegrabber.md) , чтобы получить указатель на интерфейс [**исамплеграббер**](isamplegrabber.md) . Когда средство обнаружения мультимедиа переходит в режим захвата точечного рисунка, различные информационные методы в **имедиадет** не работают.

Методы [**имедиадет:: жетбитмапбитс**](imediadet-getbitmapbits.md) или [**Имедиадет:: вритебитмапбитс**](imediadet-writebitmapbits.md) также помещают детектор мультимедиа в режим захвата точечного рисунка.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Имедиадет**](imediadet.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




