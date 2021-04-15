---
description: Метод Сетрендерранже задает диапазон времени для отрисовки на временной шкале. Объекты, находящиеся за пределами указанного диапазона, не подготавливаются к просмотру, и ресурсы не выделяются для них.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'Метод Ирендеренгине:: Сетрендерранже (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676024"
---
# <a name="irenderenginesetrenderrange-method"></a>Метод Ирендеренгине:: Сетрендерранже

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetRenderRange`Метод задает диапазон времени для отрисовки на временной шкале. Объекты, находящиеся за пределами указанного диапазона, не подготавливаются к просмотру, и ресурсы не выделяются для них.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Запуск* 
</dt> <dd>

Время начала (в 100-наносекундных единицах).

</dd> <dt>

*Остановить* 
</dt> <dd>

Время окончания (в 100-наносекундных единицах).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                            | Описание                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                   | Успешно.<br/>                            |
| <dl> <dt>**E \_ должен \_ инициализировать модуль \_ подготовки отчетов**</dt> </dl> | Не удалось инициализировать модуль визуализации.<br/> |



 

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

[**Интерфейс Ирендеренгине**](irenderengine.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




