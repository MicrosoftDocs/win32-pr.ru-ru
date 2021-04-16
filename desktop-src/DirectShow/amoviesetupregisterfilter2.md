---
description: Функция AMovieSetupRegisterFilter2 регистрирует в реестре, ПИН-коды и типы мультимедиа, с помощью интерфейса IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Функция AMovieSetupRegisterFilter2 (Дллсетуп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657837"
---
# <a name="amoviesetupregisterfilter2-function"></a>Функция AMovieSetupRegisterFilter2

Функция **AMovieSetupRegisterFilter2** регистрирует в реестре, ПИН-коды и типы мультимедиа, с помощью интерфейса [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псетупдата* 
</dt> <dd>

Указатель на данные [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) .

</dd> <dt>

*pIFM2* 
</dt> <dd>

Указатель на интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .

</dd> <dt>

*брегистер* 
</dt> <dd>

Значение, указывающее, следует ли регистрировать фильтр. **Значение true** указывает зарегистрировать фильтр, **значение false** — отменить регистрацию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Функция [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) вызывает эту вспомогательную функцию для регистрации фильтра после регистрации сервера COM.

Как правило, фильтр будет использовать [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) и не будет вызывать эту функцию напрямую.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дллсетуп. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции установки DLL**](dll-setup-functions.md)
</dt> </dl>

 

 




