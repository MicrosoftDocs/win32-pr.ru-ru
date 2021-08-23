---
description: Функция-посредник для метода Жетфриендлинаме.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: Функция IWICComponentInfo_GetFriendlyName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5af41c00945550fc9e833b9324e22f522aa7a5e73dacd109d76159d5dd0173db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965253"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>Ивиккомпонентинфо \_ жетфриендлинаме \_ -функция

Функция-посредник для метода [**жетфриендлинаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[ **ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Указатель на этот объект [**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*кчфриендлинаме* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *взфриендлинаме* .

</dd> <dt>

*взфриендлинаме* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \***

Указатель, получающий понятное имя компонента.

Возвращаемая строка зависит от языкового стандарта, 1033 по умолчанию.

</dd> <dt>

*пкчактуал* \[ заполняет\]
</dt> <dd>

Тип: **uint \***

Указатель, получающий фактическую длину понятного имени компонента.

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



 

 




