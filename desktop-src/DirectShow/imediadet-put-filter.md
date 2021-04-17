---
description: Метод размещения \_ фильтра задает фильтр источника для использования средством обнаружения мультимедиа.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'Имедиадет: метод ut_Filter:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675438"
---
# <a name="imediadetput_filter-method"></a>Имедиадет: \_ метод фильтрации:p UT

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Filter`Метод задает фильтр источника для использования средством обнаружения мультимедиа.

> [!IMPORTANT]
> Не добавляйте фильтр источника к диаграмме фильтра или используйте фильтр, который уже находится в графе фильтра. Объект детектора мультимедиа автоматически создает внутренний граф фильтра, и размещение фильтра на другом графе может привести к непредвиденным результатам.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Указатель на интерфейс **IUnknown** исходного фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения:



| Код возврата                                                                                   | Описание                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Успешно.<br/>                             |
| <dl> <dt>**\_интерфейс E**</dt> </dl> | *неввал* не указывает на фильтр.<br/> |
| <dl> <dt>**\_указатель E**</dt> </dl>     | **Пустой** аргумент указателя.<br/>           |



 

## <a name="remarks"></a>Комментарии

Для большинства приложений проще вызывать метод [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) с именем исходного файла.

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

[**Интерфейс Имедиадет**](imediadet.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




