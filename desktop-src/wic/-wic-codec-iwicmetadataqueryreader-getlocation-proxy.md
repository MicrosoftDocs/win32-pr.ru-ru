---
description: Функция-посредник для метода методического расположения.
ms.assetid: 2dc4767b-9992-4e5a-a171-2de19178d912
title: Функция IWICMetadataQueryReader_GetLocation_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetLocation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 40dd23df0e1004687a945889d2598d41ca0e2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674389"
---
# <a name="iwicmetadataqueryreader_getlocation_proxy-function"></a>\_ \_ Функция прокси Ивикметадатакуериреадер-размещения

Функция-посредник для метода методического [**расположения**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IWICMetadataQueryReader_GetLocation_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    UINT                    cchMaxLength,
  _Inout_ WCHAR                   *wzNamespace,
  _Out_   UINT                    *pcchActualLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Этот \_* \[ Вход в\]
</dt> <dd>

Тип: **[**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Указатель на этот объект [_ *ивикметадатакуериреадер* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) .

</dd> <dt>

*кчмаксленгс* \[ окне\]
</dt> <dd>

Тип: **uint**

Длина буфера *взнамеспаце* .

</dd> <dt>

*взнамеспаце* \[ в, out\]
</dt> <dd>

Тип: **WCHAR \** _

Указатель, получающий текущее расположение пространства имен.

</dd> <dt>

_pcchActualLength * \[ out\]
</dt> <dd>

Тип: **uint \** _

Фактическая длина буфера, необходимая для получения текущего расположения пространства имен.

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



 

 




