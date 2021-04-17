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
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702589"
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

Тип: **[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Указатель на этот объект [_ *ивиккомпонентинфо* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*кчфриендлинаме* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *взфриендлинаме* .

</dd> <dt>

*взфриендлинаме* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \** _

Указатель, получающий понятное имя компонента.

Возвращаемая строка зависит от языкового стандарта, 1033 по умолчанию.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Тип: **uint \** _

Указатель, получающий фактическую длину понятного имени компонента.

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



 

 




