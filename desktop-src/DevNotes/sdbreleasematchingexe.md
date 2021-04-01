---
description: Высвобождает ресурсы, используемые функцией Сдбжетматчинжексе.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Функция Сдбрелеасематчинжексе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072403"
---
# <a name="sdbreleasematchingexe-function"></a>Функция Сдбрелеасематчинжексе

Высвобождает ресурсы, используемые функцией [**сдбжетматчинжексе**](sdbgetmatchingexe.md) .

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсдб* \[ окне\]
</dt> <dd>

Маркер базы данных оболочек совместимости, возвращаемый функцией [**сдбинитдатабасе**](sdbinitdatabase.md) .

</dd> <dt>

*трексе* \[ окне\]
</dt> <dd>

[**Тагреф**](tagref.md) , возвращенный [**сдбжетматчинжексе**](sdbgetmatchingexe.md).

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

[**сдбжетматчинжексе**](sdbgetmatchingexe.md)
</dt> <dt>

[**сдбинитдатабасе**](sdbinitdatabase.md)
</dt> </dl>

 

 




