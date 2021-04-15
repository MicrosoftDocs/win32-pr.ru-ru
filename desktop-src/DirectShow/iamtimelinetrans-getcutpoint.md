---
description: Метод Жеткутпоинт извлекает вырезанную точку.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Метод Иамтимелинетранс:: Жеткутпоинт (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689449"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>Метод Иамтимелинетранс:: Жеткутпоинт

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`GetCutPoint`Метод извлекает вырезанную точку. При отрисовке перехода в виде вырезанной точки обрезка — это время, когда переход переходит от одного источника к другому. По умолчанию это значение представляет собой середину перехода. Например, в переходе, охватывающем одну секунду, вырезанная точка по умолчанию составляет 0,5 секунд в процессе перехода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птлтиме* 
</dt> <dd>

Получает вырезанную точку относительно времени начала перехода, в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** :



| Код возврата                                                                               | Описание                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Не задана вырезанная точка. Возвращаемое значение является значением по умолчанию.<br/> |
| <dl> <dt>**\_ОК**</dt> </dl>      | Для вырезанной точки задано значение, отличное от значения по умолчанию.<br/>            |
| <dl> <dt>**\_указатель E**</dt> </dl> | **Пустой** аргумент указателя.<br/>                                          |



 

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

[**Интерфейс Иамтимелинетранс**](iamtimelinetrans.md)
</dt> <dt>

[**Иамтимелинетранс:: Сеткутпоинт**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**Иамтимелинетранс:: Жеткутсонли**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**Иамтимелине:: Транситионсенаблед**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




