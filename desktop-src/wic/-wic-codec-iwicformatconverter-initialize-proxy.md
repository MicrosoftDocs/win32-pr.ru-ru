---
description: IWICFormatConverter_Initialize_Proxy функция-прокси для метода Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: Функция IWICFormatConverter_Initialize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ade363204d9edca08003d5bfef1295c4dabf52aafed037cd2e9ca69b56d02a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206533"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a>Ивикформатконвертер \_ инициализировать \_ прокси-функцию

Функция-посредник для метода [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***

Указатель на этот объект [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .

</dd> <dt>

*писаурце* \[ окне\]
</dt> <dd>

Тип: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Входной точечный рисунок для преобразования

</dd> <dt>

*дстформат* \[ окне\]
</dt> <dd>

Тип: **рефвикпикселформатгуид**

Идентификатор GUID конечного формата пикселей.

</dd> <dt>

*дизеринг* \[ окне\]
</dt> <dd>

Тип: **[ **викбитмапдисертипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**

[**Викбитмапдисертипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) , используемый для преобразования.

</dd> <dt>

*пипалетте* \[ окне\]
</dt> <dd>

Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Палитра, используемая для преобразования.

</dd> <dt>

*алфасрешолдперцент* \[ окне\]
</dt> <dd>

Тип: **Double**

Пороговое значение альфа-канала, используемое для преобразования.

</dd> <dt>

*палеттетранслате* \[ окне\]
</dt> <dd>

Тип: **[ **викбитмаппалеттетипе**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Тип перевода палитры, используемый для преобразования.

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



 

 




