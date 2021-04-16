---
description: Функция-посредник для метода Сетресолутион.
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: Функция IWICBitmapFrameEncode_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9801384e305f2449c6a31b80cb238fc92f7b63b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693172"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a>Ивикбитмапфраминкоде \_ сетресолутион \_ -функция

Функция-посредник для метода [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _

Указатель на этот объект [_ *ивикбитмапфраминкоде* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .

</dd> <dt>

*дпикс* \[ окне\]
</dt> <dd>

Тип: **Double**

Значение разрешения по горизонтали.

</dd> <dt>

*дпий* \[ окне\]
</dt> <dd>

Тип: **Double**

Значение разрешения по вертикали.

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



 

 




