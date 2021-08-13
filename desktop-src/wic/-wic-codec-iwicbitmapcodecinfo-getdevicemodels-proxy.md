---
description: Функция-посредник для метода Жетдевицемоделс.
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: Функция IWICBitmapCodecInfo_GetDeviceModels_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 659ca401384f907e0bad1a86dd79e61bad55cf2612bb45713246b26711e57d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711990"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a>ИвикбитмапкодеЦинфо \_ жетдевицемоделс \_ -функция

Функция-посредник для метода [**жетдевицемоделс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Указатель на этот объект [**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*кчдевицемоделс* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера моделей устройств.

</dd> <dt>

*вздевицемоделс* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \***

Указатель, получающий разделенный запятыми список имен моделей устройств, связанных с кодеком.

</dd> <dt>

*пкчактуал* \[ в, out\]
</dt> <dd>

Тип: **uint \***

Фактический размер буфера, необходимый для получения всех имен моделей устройств.

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



 

 




