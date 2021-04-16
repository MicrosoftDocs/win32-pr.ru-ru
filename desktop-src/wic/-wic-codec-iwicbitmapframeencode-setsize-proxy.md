---
description: Функция-посредник для метода SetSize.
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: Функция IWICBitmapFrameEncode_SetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693254"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a>Ивикбитмапфраминкоде \_ SetSize, \_ функция прокси

Функция-посредник для метода [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _

Указатель на этот объект [_ *ивикбитмапфраминкоде* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .

</dd> <dt>

*уивидс* \[ окне\]
</dt> <dd>

Тип: **uint**

Ширина выходного изображения.

</dd> <dt>

*уихеигхт* \[ окне\]
</dt> <dd>

Тип: **uint**

Высота выходного изображения.

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



 

 




