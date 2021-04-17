---
description: Метод Сетсвапинпутс указывает, меняются ли входные данные перехода.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'Метод Иамтимелинетранс:: Сетсвапинпутс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689340"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>Метод Иамтимелинетранс:: Сетсвапинпутс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`SetSwapInputs`Метод указывает, меняются ли входные данные перехода.

По умолчанию переход проходит от состава всех слоев с низким приоритетом до слоя, в котором находится переход. Эту прогрессию можно отменить, чтобы переход выполнялся с слоя, где он находится в составе слоев с более низким приоритетом. Дополнительные сведения см. в разделе [направление перехода](transition-direction.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Val* 
</dt> <dd>

Указывает, будут ли входные данные перепутаны. Если **значение равно false**, переход проходит от составного набора всех уровней с низким приоритетом до слоя перехода. Если **значение равно true**, переход проходит в обратном направлении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод не изменяет направление визуального элемента. Например, очистка слева направо будет по-прежнему идти слева направо. Чтобы изменить направление, задайте свойство **Progress** с помощью интерфейса [**ипропертисеттер**](ipropertysetter.md) .

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

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




