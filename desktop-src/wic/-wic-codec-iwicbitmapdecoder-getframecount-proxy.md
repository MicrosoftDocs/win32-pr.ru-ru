---
description: Функция-посредник для метода Жетфрамекаунт.
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: Функция IWICBitmapDecoder_GetFrameCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809580"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a>Ивикбитмапдекодер \_ жетфрамекаунт \_ -функция

Функция-посредник для метода [**жетфрамекаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _

Указатель на этот объект [_ *ивикбитмапдекодер* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .

</dd> <dt>

*pCount* \[ заполняет\]
</dt> <dd>

Тип: **uint \** _

Указатель, получающий общее число кадров в изображении.

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



 

 




