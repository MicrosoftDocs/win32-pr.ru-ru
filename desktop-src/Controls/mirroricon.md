---
title: Функция Миррорикон
description: Меняет местами значки (зеркала), чтобы они отображались правильно в контексте зеркального устройства.
ms.assetid: bca87037-1789-466b-9be0-914966fdad31
keywords:
- Элементы управления Windows для функций Миррорикон
topic_type:
- apiref
api_name:
- MirrorIcon
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f180d509464b63e5ec73c5fb74e4d70386bdea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071253"
---
# <a name="mirroricon-function"></a>Функция Миррорикон

\[**Миррорикон** доступен в Windows XP с пакетом обновления 2 (SP2). Он может быть изменен или недоступен в последующих версиях.\]

Меняет местами значки (зеркала), чтобы они отображались правильно в контексте зеркального устройства.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI MirrorIcon(
  _Inout_opt_ HICON *phIconSmall,
  _Inout_opt_ HICON *phIconLarge
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фиконсмалл* \[ в, out, необязательно\]
</dt> <dd>

Тип: **[**Хикон**](/windows/desktop/WinProg/windows-data-types) \** _

Указатель на маркер значка, который ссылается на небольшую версию значка.

</dd> <dt>

_phIconLarge * \[ в, out, необязательно\]
</dt> <dd>

Тип: **[**Хикон**](/windows/desktop/WinProg/windows-data-types) \** _

Указатель на маркер значка, который ссылается на крупную версию значка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *[**bool**](/windows/desktop/WinProg/windows-data-types)**

**Значение true** в случае успешного выполнения; в противном случае — **значение false**.

## <a name="remarks"></a>Комментарии

**Миррорикон** не экспортируется по имени или объявлено в общедоступном файле заголовка. Чтобы использовать его, необходимо использовать [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) и запросить порядковый номер 414 из ComCtl32.dll для получения указателя на функцию.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                                  |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (версия 5,81 или более поздняя)</dt> </dl> |



 

