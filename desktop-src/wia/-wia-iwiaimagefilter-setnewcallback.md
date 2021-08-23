---
description: Задает новый обратный вызов приложения для фильтра обработки изображений, используемого для переадресации вызовов.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Метод Ивиаимажефилтер:: Сетневкаллбакк (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: abb279faba1c5174fc39ebdfe30a4a8cde8cabf86e8b86599f8d3ab9cc3247cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450494"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>Метод Ивиаимажефилтер:: Сетневкаллбакк

Задает новый обратный вызов приложения для фильтра обработки изображений, используемого для переадресации вызовов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвиатрансферкаллбакк* \[ окне\]
</dt> <dd>

Тип: **[ **ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md)**

Указывает указатель на интерфейс [**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) приложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Не вызывайте этот метод непосредственно из приложения.

Фильтр обработки изображений необходим для освобождения ранее сохраненного интерфейса обратного вызова приложения перед установкой нового обратного вызова.

Если *пвиатрансферкаллбакк* имеет **значение NULL**, фильтр обработки изображений должен просто освободить Старый обратный вызов приложения и возвратить \_ ОК.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




