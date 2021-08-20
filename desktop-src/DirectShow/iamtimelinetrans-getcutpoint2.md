---
description: 'Метод GetCutPoint2 извлекает вырезанную точку. Этот метод эквивалентен Иамтимелинетранс:: Жеткутпоинт, но принимает значение РЕФТИМЕ.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'Метод Иамтимелинетранс:: GetCutPoint2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 291aff15260d5d693f3e6b0281d693a7351132fc017358f6f9ee21020dfd4f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952763"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a>Метод Иамтимелинетранс:: GetCutPoint2

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetCutPoint2`Метод извлекает вырезанную точку. Этот метод эквивалентен [**иамтимелинетранс:: жеткутпоинт**](iamtimelinetrans-getcutpoint.md), но принимает значение [**рефтиме**](reftime.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птлтиме* 
</dt> <dd>

Получает вырезанную точку относительно времени начала перехода в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                               | Описание                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Не задана вырезанная точка. Возвращаемое значение является значением по умолчанию.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>      | Для вырезанной точки задано значение, отличное от значения по умолчанию.<br/>            |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/>                                          |



 

## <a name="remarks"></a>Remarks

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

[**Интерфейс Иамтимелинетранс**](iamtimelinetrans.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




