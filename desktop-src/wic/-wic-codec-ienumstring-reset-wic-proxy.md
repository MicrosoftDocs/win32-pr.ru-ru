---
description: 'Windows Функция-посредник компонента обработки изображений (WIC) для Иенумстринг:: Reset.'
ms.assetid: 084a3de0-c6de-4ce2-ba78-5d1bacb56cb0
title: Функция IEnumString_Reset_WIC_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumString_Reset_WIC_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc06a00b5e80befe1e6a69f7c2b402597699c97bf866129ca10175e18fe34a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549624"
---
# <a name="ienumstring_reset_wic_proxy-function"></a>Иенумстринг \_ Сброс \_ \_ функции прокси-сервера WIC

Windows Функция-посредник компонента обработки изображений (WIC) для Иенумстринг:: Reset.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IEnumString_Reset_WIC_Proxy(
  _In_  IEnumString *THIS_PTR,
  _In_  ULONG       celt,
  _Out_ LPOLESTR    *rgelt,
  _Out_ ULONG       *pceltFetched
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **иенумстринг \***

парамдеск

</dd> <dt>

*celt* \[ окне\]
</dt> <dd>

Тип: **ulong**

</dd> <dt>

*rgelt* \[ заполняет\]
</dt> <dd>

Тип: **лполестр \***

</dd> <dt>

*пцелтфетчед* \[ заполняет\]
</dt> <dd>

Тип: **ulong \***

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



 

 




