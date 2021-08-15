---
description: IWICBitmapFrameEncode_Commit_Proxy функция-прокси для метода Commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: Функция IWICBitmapFrameEncode_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: af57499fb59c88d3cf8a1d0e4625550825df5f0e04245f9bec4706e602fd2006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711927"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a>Ивикбитмапфраминкоде \_ фиксация \_ прокси-функции

Функция-посредник для метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Указатель на этот объект [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .

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



 

 




