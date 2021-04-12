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
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265865"
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

Тип: **[**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _

Указатель на этот объект [_ *ивикстреам* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .

</dd> <dt>

*пистреам* \[ окне\]
</dt> <dd>

Тип: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _

Поток инициализации.

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



 

