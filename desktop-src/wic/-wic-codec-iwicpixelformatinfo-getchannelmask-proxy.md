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
ms.openlocfilehash: ee200dddf0b2cd736ca2ad435b63e774076465ad3d1f6215f1c558f1abb6c194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056604"
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

Тип: **[ **ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\***

Указатель на этот объект [**ивикпикселформатинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) .

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

Тип: **Byte \***

Указатель на буфер маски.

</dd> <dt>

*пкбактуал* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Фактический размер буфера, необходимый для получения маски канала.

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



 

 




