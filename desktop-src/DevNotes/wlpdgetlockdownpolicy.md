---
description: Вызывает библиотеку, чтобы получить состояние безопасности относительно узла и использовать скрипт или MSI.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Функция Влдпжетлоккдовнполици (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538750"
---
# <a name="wldpgetlockdownpolicy-function"></a>Функция Влдпжетлоккдовнполици

Вызывает библиотеку, чтобы получить состояние безопасности относительно узла и использовать скрипт или MSI. У функции нет связанной библиотеки импорта. Для динамической привязки к wldp.dll необходимо использовать функции LoadLibrary и GetProcAddress.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хостинформатион* \[ в необязательное\]
</dt> <dd>

Структура [**\_ \_ информации узла WLDP**](wldp-host-information.md) , определяющая узел и исходный файл для оценки.

</dd> <dt>

*локкдовнстате* \[ заполняет\]
</dt> <dd>

Предоставляет результирующее значение безопасной политики. Наличии! WLDP_LOCKDOWN_IS_OFF, то УМЦИ включен. Можно также проверить WLDP_LOCKDOWN_IS_AUDIT и WLDP_LOCKDOWN_IS_ENFORCE, чтобы определить, находится ли политика в режиме аудита или принудительного применения.
</dd> <dt>

*локкдовнфлагс* \[ окне\]
</dt> <dd>

Следующие значения флагов определены WLDP \_ flags \_ скипсигнатуревалидатион 0x00000100 — Если задано значение, пропускать проверку SaferIdentifyLevel, которая будет пропускать, подписан ли сценарий.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает \_ значение ОК в случае успеха или код ошибки в противном случае.

## <a name="remarks"></a>Комментарии

При вызове со \_ \_ сведениями об узле WLDP. СЗСАУРЦЕ = NULL возвращается универсальная политика для узла.

При вызове со \_ \_ сведениями об узле WLDP. ДВХОСТИД = WLDP \_ \_ идентификатор узла \_ Global, WLDP \_ \_ сведения об узле. сзсаурце должен иметь значение null, а функция вернет глобальную системную политику.

DwFlag WLDP \_ flags \_ скипсигнатуревалидатион можно использовать для пропуска проверки SaferIdentifyLevel (), которая будет пропускать, подписан ли скрипт.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




