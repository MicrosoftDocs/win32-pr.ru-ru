---
description: Вызывает библиотеку, чтобы проверить, является ли определенный идентификатор CLSID надежным для вызова.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Функция Влдписклассинаппроведлист (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: ef4f6a719a1fe5146badbe59239dc16f9031f553ee8bba189c838dddcb641d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642044"
---
# <a name="wldpisclassinapprovedlist-function"></a>Функция Влдписклассинаппроведлист

Вызывает библиотеку, чтобы проверить, является ли определенный **идентификатор CLSID** надежным для вызова. У функции нет связанной библиотеки импорта. Для динамической привязки к wldp.dll необходимо использовать функции LoadLibrary и GetProcAddress.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Класса* 
</dt> <dd>

Идентификатор класса COM для проверки на одобрение.

</dd> <dt>

*хостинформатион* \[ окне\]
</dt> <dd>

Структура [**\_ \_ информации узла WLDP**](wldp-host-information.md) , определяющая оцениваемый узел.

</dd> <dt>

*утверждено* \[ заполняет\]
</dt> <dd>

При успешном завершении содержит **значение true** , если идентификатор класса утвержден. в противном случае — **значение false**.

</dd> <dt>

*оптионалфлагс* 
</dt> <dd>

Этот параметр зарезервирован и должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




