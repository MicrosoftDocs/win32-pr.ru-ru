---
description: Получает системный каталог Апппатч.
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: Функция Сдбжетапппатчдир
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140742"
---
# <a name="sdbgetapppatchdir-function"></a>Функция Сдбжетапппатчдир

Получает системный каталог Апппатч.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсдб* \[ в необязательное\]
</dt> <dd>

Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .

</dd> <dt>

*сзапппатчпас* \[ заполняет\]
</dt> <dd>

Результирующий путь.

</dd> <dt>

*кчсизе* \[ окне\]
</dt> <dd>

Размер буфера *сзапппатчпас* в символах. Если функция завершается ошибкой, для этого параметра задается пустая строка ("").

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сдбинитдатабасе**](sdbinitdatabase.md)
</dt> </dl>

 

 




