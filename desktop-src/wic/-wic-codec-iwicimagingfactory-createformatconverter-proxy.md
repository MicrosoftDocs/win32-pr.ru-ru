---
description: Функция-посредник для метода Креатеформатконвертер.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: Функция IWICImagingFactory_CreateFormatConverter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9d171847df9fb3b7fdcd15960d2caa91be09a65da2c8bb4d664aa714944435b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088296"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a>IWICImagingFactory \_ креатеформатконвертер \_ -функция

Функция-посредник для метода [**креатеформатконвертер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфактори* \[ окне\]
</dt> <dd>

Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ппиформатконвертер* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***

Указатель, получающий указатель на новый [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), Windows \[ только классические приложения Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




