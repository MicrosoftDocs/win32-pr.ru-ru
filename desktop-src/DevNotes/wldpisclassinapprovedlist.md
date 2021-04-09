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
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140890"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




