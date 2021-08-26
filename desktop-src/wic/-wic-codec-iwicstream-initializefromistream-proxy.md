---
description: Функция-посредник для метода Инитиализефромистреам.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: Функция IWICStream_InitializeFromIStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 491a2a67881929eba86dc317645161dee28ee9062d01fee63a9f6d4a7995cf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056564"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a>Ивикстреам \_ инитиализефромистреам \_ -функция

Функция-посредник для метода [**инитиализефромистреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***

Указатель на этот объект [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .

</dd> <dt>

*пистреам* \[ окне\]
</dt> <dd>

Тип: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

Поток инициализации.

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



 

