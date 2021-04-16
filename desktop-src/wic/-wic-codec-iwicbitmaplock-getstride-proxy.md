---
description: Функция-посредник для метода STRIDE.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: Функция IWICBitmapLock_GetStride_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702859"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a>Ивикбитмаплокк \_ \_ -функция класса STRIDE

Функция-посредник для метода [**stride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _

Указатель на этот объект [_ *ивикбитмаплокк* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .

</dd> <dt>

*пкбстриде* \[ заполняет\]
</dt> <dd>

Тип: **uint \** _

Шаг точечного рисунка.

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



 

 




