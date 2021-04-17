---
description: Функция-посредник для метода WebMethod.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: Функция IWICComponentInfo_GetVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713120"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>\_ \_ Функция прокси Ивиккомпонентинфо-версии

Функция-посредник для [**метода WebMethod**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
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

*кчверсион* \[ окне\]
</dt> <dd>

Тип: **uint**

Размер буфера *взверсион* .

</dd> <dt>

*взверсион* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \** _

Указатель, который получает неизменяемую строку языка и региональных параметров для версии компонента.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Тип: **uint \** _

Указатель, получающий фактическую длину версии компонента.

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



 

 




