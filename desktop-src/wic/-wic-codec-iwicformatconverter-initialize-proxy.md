---
description: Функция-посредник для метода Initialize.
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
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266145"
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

Тип: **[**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _

Указатель на этот объект [_ *ивикформатконвертер* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) .

</dd> <dt>

*писаурце* \[ окне\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Входной точечный рисунок для преобразования

</dd> <dt>

_dstFormat * \[ в\]
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

Тип: **[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Палитра, используемая для преобразования.

</dd> <dt>

_alphaThresholdPercent * \[ в\]
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
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




