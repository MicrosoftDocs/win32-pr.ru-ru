---
description: Метод Жеттрансаттиме извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'Метод Иамтимелинетрансабле:: Жеттрансаттиме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689416"
---
# <a name="iamtimelinetransablegettransattime-method"></a>Метод Иамтимелинетрансабле:: Жеттрансаттиме

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetTransAtTime`Метод извлекает переход, ближайший к заданному времени, в соответствии с указанными условиями границ.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппобж* \[ заполняет\]
</dt> <dd>

Получает указатель на интерфейс [**иамтимелинеобж**](iamtimelineobj.md) перехода.

</dd> <dt>

*Time* 
</dt> <dd>

Время, с которого начинается поиск, в единицах 100-наносекундных.

</dd> <dt>

*сеарчдиректион* 
</dt> <dd>

Член перечисляемого типа [**декстерф \_ Track \_ Search \_ flags**](dexterf-track-search-flags.md) , указывающий условия границ для поиска.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                                  | Описание                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Переход не найден.<br/>   |
| <dl> <dt>**\_ОК**</dt> </dl>         | Обнаружен переход.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый аргумент.<br/>          |
| <dl> <dt>**\_указатель E**</dt> </dl>    | **Пустой** аргумент указателя.<br/> |



 

## <a name="remarks"></a>Комментарии

Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок. Не забудьте освободить интерфейс по завершении его использования.

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

 

 




