---
description: Функция-посредник для метода CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: Функция IWICBitmapSource_CopyPixels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266146"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a>IWICBitmapSource \_ CopyPixels \_ -функция

Функция-посредник для метода [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Указатель на этот объект [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*КНР* \[ окне\]
</dt> <dd>

Тип: **const [**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

Копируемый прямоугольник. Значение NULL указывает всю битовую карту.

</dd> <dt>

_cbStride * \[ в\]
</dt> <dd>

Тип: **uint**

Шаг точечного рисунка

</dd> <dt>

*кббуфферсизе* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера.

</dd> <dt>

*пббуффер* \[ заполняет\]
</dt> <dd>

Тип: **Byte \** _

Указатель на буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если эта функция завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]<br/>                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt> </dl> |



 

 




