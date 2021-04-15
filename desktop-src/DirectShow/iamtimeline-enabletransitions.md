---
description: Метод Енаблетранситионс включает или отключает все переходы на временной шкале.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Метод Иамтимелине:: Енаблетранситионс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651787"
---
# <a name="iamtimelineenabletransitions-method"></a>Метод Иамтимелине:: Енаблетранситионс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`EnableTransitions`Метод включает или отключает все переходы на временной шкале. Если переходы отключены, модули подготовки отчетов обрабатывают их как «быстрые»; Это значит, что отображаемые выходные данные быстро переходят с одной записи на другую. Точка обрезки по умолчанию находится в середине до длительности перехода. Можно изменить точку вырезания, вызвав метод [**иамтимелинетранс:: сеткутпоинт**](iamtimelinetrans-setcutpoint.md) для перехода. Отключенные переходы не удаляются с временной шкалы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фенаблед* 
</dt> <dd>

Логическое значение, указывающее, следует ли включать или отключать переходы. Если **значение равно true**, переходы включены. Если **значение равно false**, переходы отключены.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

[**Интерфейс Иамтимелине**](iamtimeline.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




