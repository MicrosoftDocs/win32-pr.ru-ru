---
description: Функция-посредник для метода Жетколорконтекстс.
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: Функция IWICBitmapFrameDecode_GetColorContexts_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e22166e98e4ef276a6bf1d72dfc860cf8fb511e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263025"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a>IWICBitmapFrameDecode \_ жетколорконтекстс \_ -функция

Функция-посредник для метода [**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _

Указатель на этот объект [_ *IWICBitmapFrameDecode* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .

</dd> <dt>

*учетная запись* \[ окне\]
</dt> <dd>

Тип: **uint**

Число извлекаемых контекстных цветов.

Это значение должно быть размером или меньше, чем размер, доступный для *ппиколорконтекстс*.

</dd> <dt>

*ппиколорконтекстс* \[ в, out\]
</dt> <dd>

Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***

Указатель, получающий указатель на объекты [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) .

</dd> <dt>

*пкактуалкаунт* \[ заполняет\]
</dt> <dd>

Тип: **uint \** _

Указатель, получающий количество цветовых контекстов, содержащихся в кадре изображения.

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



 

 




