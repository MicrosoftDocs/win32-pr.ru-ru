---
description: Функция-посредник для метода Креатебитмапфлипротатор.
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: Функция IWICImagingFactory_CreateBitmapFlipRotator_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664294"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a>IWICImagingFactory \_ креатебитмапфлипротатор \_ -функция

Функция-посредник для метода [**креатебитмапфлипротатор**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIBitmapFlipRotator * \[ out\]
</dt> <dd>

Тип: **[ **ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***

Указатель, получающий указатель на новый [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

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



 

 




