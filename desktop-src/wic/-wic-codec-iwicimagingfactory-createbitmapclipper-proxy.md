---
description: Функция-посредник для метода Креатебитмапклиппер.
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: Функция IWICImagingFactory_CreateBitmapClipper_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999256"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a>IWICImagingFactory \_ креатебитмапклиппер \_ -функция

Функция-посредник для метода [**креатебитмапклиппер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIBitmapClipper * \[ out\]
</dt> <dd>

Тип: **[ **ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***

Указатель, получающий указатель на новый [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




