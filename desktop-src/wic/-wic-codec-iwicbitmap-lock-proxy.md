---
description: Функция-посредник для метода Lock.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: Функция IWICBitmap_Lock_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 98415428a020129d884a036fab121511e489ec96af3a5606e25283dfec69c21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207235"
---
# <a name="iwicbitmap_lock_proxy-function"></a>Ивикбитмап \_ Lock \_ -функция

Функция-посредник для метода [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***

Указатель на этот объект [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .

</dd> <dt>

*прклокк* \[ окне\]
</dt> <dd>

Тип: **const [**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***

Прямоугольник, к которому осуществляется доступ.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Режим доступа, который вы хотите получить для блокировки.

</dd> <dt>

*ппилокк* \[ заполняет\]
</dt> <dd>

Тип: **[ **ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***

Указатель, получающий заблокированную область памяти.

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



 

 




