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
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044994"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




