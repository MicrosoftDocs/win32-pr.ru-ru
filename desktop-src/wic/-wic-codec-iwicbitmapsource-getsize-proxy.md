---
description: Функция-посредник для метода методом Resize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: Функция IWICBitmapSource_GetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702401"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a>IWICBitmapSource \_ \_ -функция @ size

Функция-посредник для метода методом [**resize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Указатель на этот объект [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*пуивидс* \[ заполняет\]
</dt> <dd>

Тип: **uint \** _

Указатель, получающий ширину точечного рисунка в пикселях.

</dd> <dt>

_puiHeight * \[ out\]
</dt> <dd>

Тип: **uint \** _

Указатель, который получает высоту точечного рисунка в пикселях

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



 

 




