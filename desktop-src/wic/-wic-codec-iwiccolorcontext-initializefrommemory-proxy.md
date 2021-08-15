---
description: IWICColorContext_InitializeFromMemory_Proxy функция-прокси для метода Инитиализефроммемори.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: Функция IWICColorContext_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e662e4a88858d413636289e6418e38fb1a1fe0bb864620d029cc8975bde7278f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711475"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a>Ивикколорконтекст \_ инитиализефроммемори \_ -функция

Функция-посредник для метода [**инитиализефроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

</dd> <dt>

*пббуффер* \[ окне\]
</dt> <dd>

Тип: **Константный \* байт**

Буфер, используемый для инициализации [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).

</dd> <dt>

*кббуфферсизе* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *пббуффер* .

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



 

 




