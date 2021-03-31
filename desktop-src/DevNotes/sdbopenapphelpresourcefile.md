---
description: Загружает файл ресурсов AppHelp.
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: Функция Сдбопенапфелпресаурцефиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2f1dfb1695e25bfb82e01ffa4f9eac4e245a6ffa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423345"
---
# <a name="sdbopenapphelpresourcefile-function"></a>Функция Сдбопенапфелпресаурцефиле

Загружает файл ресурсов AppHelp.

## <a name="syntax"></a>Синтаксис


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсзакресаурцефиле* \[ в необязательное\]
</dt> <dd>

Путь к файлу ресурсов. Если этот параметр имеет **значение NULL**, то открывается Локальная библиотека ресурсов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает маркер в открытый файл ресурсов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




