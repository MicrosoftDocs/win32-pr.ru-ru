---
description: Функция-посредник для метода Жетчаннелмаск.
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: Функция IWICPixelFormatInfo_GetChannelMask_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272303"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a>Ивикпикселформатинфо \_ жетчаннелмаск \_ -функция

Функция-посредник для метода [**жетчаннелмаск**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

Указатель на этот объект [_ *ивикпикселформатинфо* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

</dd> <dt>

*уичаннелиндекс* \[ окне\]
</dt> <dd>

Тип: **uint**

Индекс для извлекаемой маски канала.

</dd> <dt>

*кбмаскбуффер* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *пбмаскбуффер* .

</dd> <dt>

*пбмаскбуффер* \[ в, out\]
</dt> <dd>

Тип: **Byte \** _

Указатель на буфер маски.

</dd> <dt>

_pcbActual * \[ out\]
</dt> <dd>

Тип: **uint \** _

Фактический размер буфера, необходимый для получения маски канала.

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



 

 




